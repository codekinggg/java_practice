package ch01_02_03;

import java.util.Scanner;

public class _ericKim_0802 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner in = new Scanner(System.in);
		int i;
		
		System.out.print("학번은? ");
		String st_num = in.next();
		
		System.out.println("입학 연도: " + st_num.charAt(2) + st_num.charAt(3));
		System.out.println("입학 유형: " + st_num.charAt(4));
		System.out.print("입학 순번: ");
		for(i=5; i< st_num.length(); i++) {
		System.out.print(st_num.charAt(i));
		}
		System.out.println();
		
		if(st_num.length() != 8) {
			System.out.println("틀린 이유: 길이가 8이 아니다.");
		}
		if(st_num.charAt(0) != '6' || st_num.charAt(1) != '0') {
			System.out.println("틀린 이유: 60으로 시작하지 않는다.");
		}
		if(st_num.charAt(4) != '2' && st_num.charAt(4) != '5') {
			System.out.println("틀린 이유: 입학 유형");
		}
		if(st_num.length() >= 9) {
			System.out.println("틀린 이유: 입학 순번");
		}
		
		if(st_num.length() == 8 && (st_num.charAt(0) == '6' || st_num.charAt(1) == '0')) {
			if(st_num.charAt(4) == '2' || st_num.charAt(4) == '5') {
				System.out.println("학번이 맞다.");
			}
		}
		in.close();
	}

}
