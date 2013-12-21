package General;
/*
 * @Author Emre
 * */
public class DrawHome {
	private int width,height,roof_height,center,door_width, door_height,med_height;

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		DrawHome draw = new DrawHome(45);
		draw.drawRoof();
		draw.drawMed();
		draw.drawDoor();
		
	}
	
	public DrawHome(int width){
		this.width = width;
		this.height = this.center = width/2;
		this.roof_height = this.door_width = (this.height/2)+1;
		this.door_height = (this.door_width/2)+1;
		int start_width = (this.center-this.door_width)/2;
		this.med_height = this.height - (start_width+this.door_height);
	}

	public void drawRoof(){
		int space = this.center;
		int limit = 2;
		for(int i = 1; i <= this.roof_height; i++){
			drawSpace(space);
			if(space != this.center){
				for(int j = 1; j <limit; j++){
					if((limit / 2) == j){
						System.out.print("+");
					}else if(limit / 2 < j){
						System.out.print("\\");
					}else{
						System.out.print("/");
					}
				}
			}else{
				System.out.print("+");
			}
			
			limit = limit+4;
			space = space - 2;
			System.out.println();
		}
		
	}
	public void drawSpace(int count){
		for(int i = count; i > 0; i--){
			System.out.print(" ");
		}
	}
	public void drawMed(){

		int start = (this.center-this.door_width)/2;
		for(int i = 1; i <= this.med_height-this.door_height; i++){
			for(int j = 1; j <= this.width; j++){
				System.out.print("0");
			}
			System.out.println();
		}
		for(int i = 1; i <= this.door_height; i++){
	
			for(int j = 1; j <= this.width; j++){
					
					if(j < center){ // Left
						
						if(j > start && j <= start+this.door_width){
							if(this.door_width == j){ // Merkez
								System.out.print("*");
							}else if(average(this.door_height,1) == i){
								System.out.print("*");
							}else{
								System.out.print(" ");
							}
						}else{ // 000
							System.out.print("0");
							
									
						}
					
					}else if(j == center){
						System.out.print("0");
					}else{ // Right
						
						if(j > center+start+1 && j <= (center+start+this.door_width)+1){
							if(center+this.door_width+1 == j){ // Merkez
								System.out.print("*");
							}else if(average(this.door_height,1) == i){
								System.out.print("*");
							}else{
								System.out.print(" ");
							}
						}else{ // 000
							System.out.print("0");
						}
						
					}
					
				}
			
			System.out.println();
		}
		
		
	}
	public void drawDoor(){
		int start_width = (this.center-this.door_width)/2;
		for(int i = 1; i <=start_width+this.door_height; i++){
			
			if(i >= this.door_height){
			
			for(int j = 0; j <this.width; j++){
				
				if(j >= center-start_width && j <= center+start_width){
					if(j == center){
						System.out.print("*");
					}else{
						System.out.print(" ");
					}
				}else{
					System.out.print("0");
				}
				
			}}
			else{
				for(int j = 0; j <this.width; j++){
					System.out.print("0");
				}
			}
			System.out.println();
		}
		
		
	}
	
	public int average(int a, int b){
		
		while(--a > ++b);
		return a;
	}
	

}
