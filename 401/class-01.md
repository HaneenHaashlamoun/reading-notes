# A beginner's guide to Big O 
![o](https://www.educative.io/v2api/editorpage/5870871921033216/image/6036875259150336)

-----------------------------------------

![summery](https://images.squarespace-cdn.com/content/v1/506e28cee4b04973cff61716/1368307616176-E6KM0CS5ODO33AV7LWYT/Big+O+Notation+Summary.jpg)

-----------------------------------------

### O(1)

>`bool IsFirstElementNull(IList<String> elements)`
>`{`
>`   return elements[0] == null;`
>`}`

### O(N)

>`bool ContainsValue(IEnumerable<string> elements, string value)`
>`{`
>`    foreach (var element in elements)`
>`    {`
>`        if (element == value) return true; `
>`    }     `
>`    return false; `
>`}`

### O(N²)

>`bool ContainsDuplicates(IList<string> elements)`
>`{`
>`    for (var outer = 0; outer < elements.Count; outer++) `
>`    {`
>`        for (var inner = 0; inner < elements.Count; inner++) `
>`        { `
>`            // Don't compare with self `
>`            if (outer == inner) continue;`            
>`            if (elements[outer] == elements[inner]) return true; `
>`        }`
>`    }    `
>`    return false;`
>`}`

### O(2^N)

>`int Fibonacci(int number)`
>`{`
>`    if (number <= 1) return number;`       
>`    return Fibonacci(number - 2) + Fibonacci(number - 1); `
>`}`

-------------------------


![chart](https://miro.medium.com/max/1147/1*ENi6u9Dles2KegA8_XfuCA.png)

-------------------------


For more info watch this video :Facts and Myths about Python names and values

[![python basics](https://nedbatchelder.com/text/names1_pix/007.png)](https://www.youtube.com/watch?v=_AEJHKGk9ns)


© Haneen Hashlamoun
