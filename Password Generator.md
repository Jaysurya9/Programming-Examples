## Python Random Password Generator Code

    import string
    import random
    characters = string.ascii_letters + string.punctuation  + string.digits

    password = ""
    password_length = random.randint(8, 16)

    for i in range(password_length):
        char = random.choice(characters)
        password = password + char

    print(password)

## JavaScript Random Password Generator Code

    function generatePassword() {
        var length = 8,
        charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789",          retVal = "";
        for (var i = 0, n = charset.length; i < length; ++i) {
            retVal += charset.charAt(Math.floor(Math.random() * n));
        }
        return retVal;
    }

## Swift Random Password Generator Code
    
    let passwordCharacters = Array("abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890".characters)
    let len = 8
    var password = ""
    
    for i in 0..
        let rand = arc4random_uniform(UInt32(passwordCharacters.count))
        password.append(passwordCharacters[Int(rand)])
    }
    print(password)

    let pswdChars = Array("abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890")
    let rndPswd = String((0..print(rndPswd)
    let len = 8
    let pswdChars ="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890"
    let rndPswd = String((0..print(rndPswd)
