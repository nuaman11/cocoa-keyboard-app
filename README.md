# cocoa-keyboard-app

import UIKit

class ViewController: UIViewController,UITextFieldDelegate {

    @IBOutlet weak var txtName: UITextField!
    @IBOutlet weak var txtMobile: UITextField!
    @IBOutlet weak var txtEmail: UITextField!
    @IBOutlet weak var txtUsername: UITextField!
    @IBOutlet weak var txtPassword: UITextField!
    
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
    }

    func textFieldShouldReturn(_ textField: UITextField) -> Bool {
        if textField == txtName {
            txtMobile.becomeFirstResponder()
        }else if textField == txtMobile{
            txtEmail.becomeFirstResponder()
        }else if textField == txtEmail{
            txtUsername.becomeFirstResponder()
        }else if textField == txtPassword{
        textField.resignFirstResponder()
    }

         return true
        
    }
    override func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?) {
        self.view.endEditing(true)
    }
}
