package jfx;
import javafx.application.*;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.image.Image;
import javafx.scene.image.ImageView;
import javafx.scene.layout.BorderPane;
import javafx.scene.layout.HBox;
import javafx.stage.Stage;

public class SecondJFX extends Application{

	public static void main(String[] args) {
		launch();
		
	}

	@Override
	public void start(Stage primaryStage) throws Exception {
	
		//Create nodes
		Image im = new Image("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTLnIzSkGUb9uA6FyzXBAh4rQOGJMYQ0XncBw&usqp=CAU");
		ImageView iv = new ImageView(im);
		
		iv.setFitHeight(500);
		iv.setFitWidth(400);
		
		Button hide = new Button("Hide");
		hide.setOnAction(new EventHandler<ActionEvent>(){
			public void handle(ActionEvent ae) {
				iv.setVisible(false);
			}
		});
		
		Button show = new Button("Show");
		show.setOnAction(new EventHandler<ActionEvent>() {
			public void handle(ActionEvent ae) {
				iv.setVisible(true);
			}
		});
		
		Button rotate = new Button("Rotate");
		rotate.setOnAction(new EventHandler<ActionEvent>() {
			public void handle(ActionEvent ae) {
				iv.setRotate(90);
			}
		});
		
		Button exit = new Button("Exit");
		exit.setOnAction(new EventHandler<ActionEvent>() {
			public void handle(ActionEvent ae) {
				System.exit(0);
			}
		});
		
		//Create Layout Managers
		/*HBox hb = new HBox(10);
		hb.getChildren().addAll(iv, hide, show, rotate, exit);*/
		BorderPane bp = new BorderPane();
		bp.setCenter(iv);
		bp.setLeft(show);
		bp.setRight(hide);
		bp.setTop(rotate);
		bp.setAlignment(rotate, Pos.TOP_CENTER);
		bp.setBottom(exit);
		
		//Create Scene and main layout
		Scene scene = new Scene(bp);
		
		//Add scene to stage
		primaryStage.setScene(scene);
		//Show the stage
		primaryStage.show();
	}

}
