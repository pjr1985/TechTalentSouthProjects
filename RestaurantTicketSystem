//Simple restaurant ordering system that allows for order input by a server and viewing/deleting by kitchen staff.

import java.util.LinkedList;
import java.util.Queue;
import java.util.Scanner;

public class KitchenView {
	public static void main(String[] args) {
		Scanner in = new Scanner(System.in);
		Queue<Order> orders = new LinkedList<Order>();
		
		System.out.println("Welcome to order entry: ");
		while(true) {
			System.out.print("Select an action (a/r): "); //where a= add order and r= return/read order
			String userInput = in.nextLine();
			
			if (userInput.equals("a")) {
				Order orderIn = new Order();
				
				System.out.print("Enter entree: ");
				String entree = in.nextLine();
				orderIn.setEntree(entree);
				
				System.out.print("Enter side: ");
				String side = in.nextLine();
				orderIn.setSide(side);
				
				System.out.print("Enter notes: ");
				String notes = in.nextLine();
				orderIn.setNotes(notes);
				
				orders.add(orderIn);
				
				System.out.println("------------------");
				
				int prepTime = (7 + orders.size() * 3);
				System.out.println("Estimated prep time is: " + prepTime + " minutes.");
				System.out.println();
				
			}
			else {
				
				if (orders.peek() != null) {
				Order orderOut=orders.remove();
				
				System.out.println("---------------");
				System.out.println("Entree: " + orderOut.getEntree());
				System.out.println("Side: " + orderOut.getSide());
				
				if (orderOut.getNotes().length() != 0) {
				System.out.println("Notes: " + orderOut.getNotes());
				}
				System.out.println("---------------");
				
				int remaining = orders.size();
				
				if (remaining == 1) {
					System.out.println("There is " + remaining + " order remaining.");
				}
				else if (remaining > 1){
				System.out.println("There are " + remaining + " orders remaining.");
				}
				
				else {
					System.out.println("No orders in queue! (Go take a break :) )");
				}
			}
		}
			System.out.println();
	}
}
}



public class Order {
	private String entree;
	private String side;
	private String notes;
	
	
	
	public String getEntree() {
		return entree;
	}
	public void setEntree(String entree) {
		this.entree = entree;
	}
	public String getSide() {
		return side;
	}
	public void setSide(String side) {
		this.side = side;
	}
	public String getNotes() {
		return notes;
	}
	public void setNotes(String notes) {
		this.notes = notes;
	}
}

