// import java.io.*;
// import java.text.*;
// import java.util.*;

// public class StudentList {
// 	public static void main(String[] args) {

// 		// Check arguments
// 		if (args[0].equals("a")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				BufferedReader s = new BufferedReader(
// 						new InputStreamReader(
// 								new FileInputStream("students.txt")));
// 				String r = s.readLine();
// 				String i[] = r.split(",");
// 				for (String j : i) {
// 					System.out.println(j);
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].equals("r")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				BufferedReader s = new BufferedReader(
// 						new InputStreamReader(
// 								new FileInputStream("students.txt")));
// 				String r = s.readLine();
// 				System.out.println(r);
// 				String i[] = r.split(",");
// 				Random x = new Random();
// 				int y = x.nextInt();
// 				System.out.println(i[y]);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("+")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				BufferedWriter s = new BufferedWriter(
// 						new FileWriter("students.txt", true));
// 				String t = args[0].substring(1);
// 				Date d = new Date();
// 				String df = "dd/mm/yyyy-hh:mm:ss a";
// 				DateFormat dateFormat = new SimpleDateFormat(df);
// 				String fd = dateFormat.format(d);
// 				s.write(", " + t + "\nList last updated on " + fd);
// 				s.close();
// 			} catch (Exception e) {
// 			}

// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("?")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				BufferedReader s = new BufferedReader(
// 						new InputStreamReader(
// 								new FileInputStream("students.txt")));
// 				String r = s.readLine();
// 				String i[] = r.split(",");
// 				boolean done = false;
// 				String t = args[0].substring(1);
// 				for (int idx = 0; idx < i.length && !done; idx++) {
// 					if (i[idx].equals(t)) {
// 						System.out.println("We found it!");
// 						done = true;
// 					}
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("c")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				BufferedReader s = new BufferedReader(
// 						new InputStreamReader(
// 								new FileInputStream("students.txt")));
// 				String D = s.readLine();
// 				char a[] = D.toCharArray();
// 				boolean in_word = false;
// 				int count = 0;
// 				for (char c : a) {
// 					if (c == ' ') {
// 						if (!in_word) {
// 							count++;
// 							in_word = true;
// 						} else {
// 							in_word = false;
// 						}
// 					}
// 				}
// 				System.out.println(count + " word(s) found " + a.length);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		}
// 	}
// }
// step2
// import java.io.*;
// import java.text.*;
// import java.util.*;

// public class StudentList {
// 	public static void main(String[] args) {

// 		// Check arguments
// 		if (args.length == 0) {
// 			System.out.println("No arguments provided.");
// 			return;
// 		}

// 		if (args[0].equals("a")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader s = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String r = s.readLine();
// 				String i[] = r.split(",");
// 				for (String j : i) {
// 					System.out.println(j);
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].equals("r")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader s = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String r = s.readLine();
// 				String i[] = r.split(",");
// 				Random x = new Random();
// 				int y = x.nextInt(i.length);
// 				System.out.println(i[y]);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("+")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedWriter s = new BufferedWriter(
// 					new FileWriter("students.txt", true))) {
// 				String t = args[0].substring(1);
// 				Date d = new Date();
// 				String df = "dd/MM/yyyy-hh:mm:ss a";
// 				DateFormat dateFormat = new SimpleDateFormat(df);
// 				String fd = dateFormat.format(d);
// 				s.write(", " + t + "\nList last updated on " + fd);
// 			} catch (Exception e) {
// 			}

// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("?")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader s = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String r = s.readLine();
// 				String i[] = r.split(",");
// 				boolean done = false;
// 				String t = args[0].substring(1);
// 				for (int idx = 0; idx < i.length && !done; idx++) {
// 					if (i[idx].equals(t)) {
// 						System.out.println("We found it!");
// 						done = true;
// 					}
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("c")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader s = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String D = s.readLine();
// 				char a[] = D.toCharArray();
// 				boolean in_word = false;
// 				int count = 0;
// 				for (char c : a) {
// 					if (c == ' ') {
// 						if (!in_word) {
// 							count++;
// 							in_word = true;
// 						} else {
// 							in_word = false;
// 						}
// 					}
// 				}
// 				System.out.println(count + " word(s) found " + a.length);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		}
// 	}
// }
// step3
// import java.io.*;
// import java.text.*;
// import java.util.*;

// public class StudentList {
// 	public static void main(String[] args) {

// 		// Check arguments
// 		if (args.length == 0) {
// 			System.out.println("No arguments provided.");
// 			return;
// 		}

// 		if (args[0].equals("a")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader reader = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String line = reader.readLine();
// 				String[] students = line.split(",");
// 				for (String student : students) {
// 					System.out.println(student);
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].equals("r")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader reader = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String line = reader.readLine();
// 				String[] students = line.split(",");
// 				Random random = new Random();
// 				int randomIndex = random.nextInt(students.length);
// 				System.out.println(students[randomIndex]);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("+")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedWriter writer = new BufferedWriter(
// 					new FileWriter("students.txt", true))) {
// 				String newStudent = args[0].substring(1);
// 				Date now = new Date();
// 				String dateFormatPattern = "dd/MM/yyyy-hh:mm:ss a";
// 				DateFormat dateFormat = new SimpleDateFormat(dateFormatPattern);
// 				String formattedDate = dateFormat.format(now);
// 				writer.write(", " + newStudent + "\nList last updated on " + formattedDate);
// 			} catch (Exception e) {
// 			}

// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("?")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader reader = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String line = reader.readLine();
// 				String[] students = line.split(",");
// 				boolean found = false;
// 				String searchStudent = args[0].substring(1);
// 				for (int idx = 0; idx < students.length && !found; idx++) {
// 					if (students[idx].equals(searchStudent)) {
// 						System.out.println("We found it!");
// 						found = true;
// 					}
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("c")) {
// 			System.out.println("Loading data ...");
// 			try (BufferedReader reader = new BufferedReader(
// 					new InputStreamReader(
// 							new FileInputStream("students.txt")))) {
// 				String line = reader.readLine();
// 				char[] chars = line.toCharArray();
// 				boolean inWord = false;
// 				int wordCount = 0;
// 				for (char ch : chars) {
// 					if (ch == ' ') {
// 						if (!inWord) {
// 							wordCount++;
// 							inWord = true;
// 						} else {
// 							inWord = false;
// 						}
// 					}
// 				}
// 				System.out.println(wordCount + " word(s) found " + chars.length);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		}
// 	}
// }
// step4
// import java.io.*;
// import java.text.*;
// import java.util.*;

// public class StudentList {

// 	private static String readStudentFile() throws IOException {
// 		try (BufferedReader reader = new BufferedReader(
// 				new InputStreamReader(
// 						new FileInputStream("students.txt")))) {
// 			return reader.readLine();
// 		}
// 	}

// 	private static void appendToStudentFile(String content) throws IOException {
// 		try (BufferedWriter writer = new BufferedWriter(
// 				new FileWriter("students.txt", true))) {
// 			writer.write(content);
// 		}
// 	}

// 	public static void main(String[] args) {

// 		// Check arguments
// 		if (args.length == 0) {
// 			System.out.println("No arguments provided.");
// 			return;
// 		}

// 		if (args[0].equals("a")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				String line = readStudentFile();
// 				String[] students = line.split(",");
// 				for (String student : students) {
// 					System.out.println(student);
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].equals("r")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				String line = readStudentFile();
// 				String[] students = line.split(",");
// 				Random random = new Random();
// 				int randomIndex = random.nextInt(students.length);
// 				System.out.println(students[randomIndex]);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("+")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				String newStudent = args[0].substring(1);
// 				Date now = new Date();
// 				String dateFormatPattern = "dd/MM/yyyy-hh:mm:ss a";
// 				DateFormat dateFormat = new SimpleDateFormat(dateFormatPattern);
// 				String formattedDate = dateFormat.format(now);
// 				appendToStudentFile(", " + newStudent + "\nList last updated on " + formattedDate);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("?")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				String line = readStudentFile();
// 				String[] students = line.split(",");
// 				boolean found = false;
// 				String searchStudent = args[0].substring(1);
// 				for (int idx = 0; idx < students.length && !found; idx++) {
// 					if (students[idx].equals(searchStudent)) {
// 						System.out.println("We found it!");
// 						found = true;
// 					}
// 				}
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		} else if (args[0].contains("c")) {
// 			System.out.println("Loading data ...");
// 			try {
// 				String line = readStudentFile();
// 				char[] chars = line.toCharArray();
// 				boolean inWord = false;
// 				int wordCount = 0;
// 				for (char ch : chars) {
// 					if (ch == ' ') {
// 						if (!inWord) {
// 							wordCount++;
// 							inWord = true;
// 						} else {
// 							inWord = false;
// 						}
// 					}
// 				}
// 				System.out.println(wordCount + " word(s) found " + chars.length);
// 			} catch (Exception e) {
// 			}
// 			System.out.println("Data Loaded.");
// 		}
// 	}
// }
