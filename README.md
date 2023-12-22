# Basic-ml
import UIKit

class ViewController: UIViewController {
    
    @IBOutlet weak var button1: UIButton!
    @IBOutlet weak var button2: UIButton!
    @IBOutlet weak var button3: UIButton!

    @IBOutlet weak var imageView: UIImageView!
    @IBOutlet weak var label: UILabel!

    override func viewDidLoad() {
        super.viewDidLoad()
        let imageName = "DefaultImage"
        let imageText = "Default Text"
        imageView.image = UIImage(named: imageName)
        label.text = imageText
        // Create an IBOutlet for each button
        button1.addTarget(self, action: #selector(button1Pressed), for: .touchUpInside)
        button2.addTarget(self, action: #selector(button2Pressed), for: .touchUpInside)
        button3.addTarget(self, action: #selector(button3Pressed), for: .touchUpInside)
    }

    // Define an IBAction for each button
    @IBAction func button1Pressed(_ sender: UIButton) {
        let imageName = "Frog"
        let imageText = "Frog"
        displayImageAndText(imageName: imageName, imageText: imageText)
    }
    
    #imageLiteral(resourceName: "Frog-tree.jpg"
    #imageLiteral(resourceName: "lion-png-26.png")
    #imageLiteral(resourceName: "rabbit.jpeg")
    @IBAction func button2Pressed(_ sender: UIButton) {
        let imageName = "Lion"
        let imageText = "Lion"
        displayImageAndText(imageName: imageName, imageText: imageText)
    }

    @IBAction func button3Pressed(_ sender: UIButton) {
        let imageName = "Rabbit"
        let imageText = "Rabbit"
        displayImageAndText(imageName: imageName, imageText: imageText)
    }

    // Create a function to display the image and text
    func displayImageAndText(imageName: String, imageText: String) {
        let image = UIImage(named: imageName)
        imageView.image = image
        label.text = imageText
    }
