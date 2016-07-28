# reverse
	System.out.println("enter the string");
		String s1 = ab.next();
		int c = 0, k = 0;
		int z;
	    StringBuffer s2 = new StringBuffer(s1);
		char[] array = new char[] { 'a', 'e', 'i', 'o', 'u' };
		//System.out.println(array.length);
		for (int i = 0; i < s1.length(); i++) {
			for (int j = 0; j < array.length; j++) {
				if (s1.charAt(i) == array[j]) {
					c++;
				}
			}
		}
		char[] arr = new char[s1.length()-c];
		if (c > 0) {
			for (int i = 0; i < s1.length(); i++) {
				z = 0;
				for (int j = 0; j < array.length; j++) {
					if (s2.charAt(i) == array[j]) {
						z = 1;
						continue;
					}
				}
				if (z == 0) {
					arr[k] = s2.charAt(i);
					//System.out.println(arr[k]);
					k++;
				}
			}
			String output = new String(arr);
			StringBuffer s3 = new StringBuffer(output);
			s3.reverse();
			System.out.println(s3);
		} 
		else {
			s2.reverse();
			System.out.println(s2);
		}

		ab.close();
	}

}
