# LifesavingFix

package jp.co.fl.superintro.ch09;

import java.util.Scanner;

public class LifesavingFix {
	
	private static int count;

	public static void main(String[]args) {
		
		Scanner sc = new Scanner(System.in);
		
		String read ="断に自信がない場合は最悪を想定して動きましょう。想定訓練やり直し";
		
		while(true) {
	        
			//安全の確認
			System.out.println("*************************");
			System.out.println("人が倒れています");
			System.out.println("そこは安全はですか？>【Y/N】");
			String select1 = sc.nextLine();
			
			if(select1.equals("Y")) {
				System.out.println("近づいて反応を確認しましょう");
				
				// 反応の確認
				System.out.println("*************************");
				System.out.println("呼びかけに反応にありますか？>【Y/N】");
				String select2 = sc.nextLine();
				if(select2.equals("Y")) {
					System.out.println("怪我や病気の可能性がある場合119番通報をしましょう");
					break;
				}else if(select2.equals("N")) {
					System.out.println("大声で応援を呼び、119番通報とAED手配を依頼しましょう。");
					System.out.println("通信指令員の指導に従うこと");
					
					//呼吸の確認
					System.out.println("*************************");
					System.out.println("呼吸はありますか？>【Y/N】");
					String select3 = sc.nextLine();
					if(select3.equals("Y")) {
						System.out.println("倒れている人を回復体位に変換させましょう。回復体位がわからない場合はググりましょう。");
						break;
					}else if(select3.equals("N")) {
						System.out.println("胸骨圧迫を開始しましょう。ポイントは以下の3つ");
						System.out.println("１：深さは約5cm");
						System.out.println("２：速さは100〜120回/分");
						System.out.println("３：絶え間なく");
						System.out.println("※人工呼吸は技術と意思があれば行ってください（1秒に1回を2回）");
						System.out.println("※胸骨圧迫と人工呼吸の比30：2で行うこと");
						
						//AED
						System.out.println("*************************");
						System.out.println("AEDが到着しました");
						System.out.println("AEDは自動音声のため、音声に従って使えば誰でも使用できるので安心してください");
						System.out.println("");
						System.out.println("AEDを貼る時の注意点3つ");
						System.out.println("1：体表面の汗を付属のタオル等で拭き取る");
						System.out.println("2：調布薬がある場合は剥がして体表面を拭き取る");
						System.out.println("3：ペースメーカーがある場合そこを数センチ避けて貼る");
						System.out.println("");
						
						//AED電気ショックメッセージ
						while(true) {
							
						    System.out.println("*************************");
						    System.out.println("電気ショックが必要とメッセージが流れた>【Y/N】");
						    String select4 = sc.nextLine();
						    if(select4.equals("Y")) {
						    	count++;
						    	System.out.println("周囲を確認して安全確認後、ボタンを押すこと");
						    	System.out.println(count+"回目の電気ショックを実行しました。");
						    	System.out.println("引続き胸骨圧迫と人工呼吸を繰り返しましょう。");
						    	
						    }else {
						    	System.out.println("電気ショックの必要はありませんので引続き胸骨圧迫と人工呼吸を実施してください。");
						    	break;
						    }
						}
						
						System.out.println("救急隊に引き継ぐまで、または傷病者に普段通りの呼吸や目的のある仕草が認められるまで続けること");
						System.out.println("電気ショックを打った場合は回数を救急隊に報告しましょう");
						break;
						
					}else {
						System.out.println(read);
					}
					
				}else {
					System.out.println(read);
				}
				
			}else {
				System.out.println("危険なため、119番通報をして消防の到着を待ちましょう");
				break;
			}
		}	
		
	}
}
