#Handle Go Button Action

```Swift
import UIKit

class ViewController: UIViewController, UITextFieldDelegate {

    @IBOutlet var myTextField : UITextField
                            
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
        
        self.myTextField.delegate = self;
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    func textFieldShouldReturn(textField: UITextField!) -> Bool {
        //self.view.endEditing(true);
        //return false;
        if (textField.returnKeyType==UIReturnKeyType.Go)
		{
			hideKeyboard();
			validator.validate(self)
		}
		return true
    }
}
```
