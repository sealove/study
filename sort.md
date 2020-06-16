	func selectSort(_ nums: inout [Int]) {
        for i in 0..<nums.count {
            var min = nums[i]
            var minIndex = i
            var j = i+1
            while j < nums.count {
                if nums[j] < min {
                    min = nums[j]
                    minIndex = j
                }
                j += 1
            }
            print("swap \(i):\(nums[i]) \(minIndex):\(nums[minIndex])")
            nums.swapAt(i, minIndex)
            print("\(nums)")
        }
        
    }
	
	func insertSort(_ nums:inout [Int]) {
	        for i in 1..<nums.count  {
	            let key = nums[i]
	            var j = i-1
	            for c in (0...i-1).reversed() {
	                j = c
	                print("key \(i):\(key) compare num \(j):\(nums[j])")
	                if key < nums[j] {
	                    nums[j+1] = nums[j]
	                    print("move \(nums)")
	                }
	                else {
	                    print("stop")
	                    j = j+1
	                    break
	                }
	            }
	            nums[j] = key
	            print("loop \(nums)")
	        }
	    }