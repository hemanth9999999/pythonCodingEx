dictA={ "key":"a",
  "key1":{
		"b":"c",
		"d":"e"
		},
	"key2":{
		"e":"f",
		"g":{
			"h":"i",
			"j":"k",
			"l":"m"
            }
    }
}


def flatten_dict(dictA): 
    stack=[]
    resDict={}
    def dfs(dictA): 
        for keyVal  in dictA : 
            if (not isinstance(dictA[keyVal] , dict )) : 
                keyPrefix="".join(stack)
                resDict[keyPrefix+keyVal]=dictA[keyVal]
            else: 
                stack.append(keyVal+".")
                dfs(dictA[keyVal])
                stack.pop()
    dfs(dictA)
    return resDict
