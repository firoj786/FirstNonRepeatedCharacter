# FirstNonRepeatedCharacter


    String inputString = "programmingp";
		int firstNonRepeated = inputString.chars().filter(c -> inputString.indexOf(c) == inputString.lastIndexOf(c))
				.findFirst().orElse(-1); // Use -1 to indicate no non-repeated character
		
		//inputString.chars(): Converts the string into an IntStream of characters.
		//.filter(c -> inputString.indexOf(c) == inputString.lastIndexOf(c)): Filters out characters 
		//that have the same first and last occurrence, leaving only non-repeated characters.
		//.findFirst().orElse(-1): Finds the first non-repeated character in the filtered stream or returns -1 if no non-repeated character is found.

		if (firstNonRepeated != -1) {
			char firstNonRepeatedChar = (char) firstNonRepeated;
			System.out.println("First non-repeated character: " + firstNonRepeatedChar);
		} else {
			System.out.println("No non-repeated characters found");
   
		  //	If firstNonRepeated is not equal to -1, it means a non-repeated character was found.
			//The non-repeated character is converted from its ASCII code to a char and printed to the console.
			//If firstNonRepeated is -1, it means no non-repeated character was found, and a corresponding message is printed.
		}
