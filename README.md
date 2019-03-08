# CustomNaviBar_ios

#### 내비게이션 타이틀 커스텀 1

```swift
    func initTitle(){
        //1. 내비게이션 타이틀용 레이블 객체
        let nTitle = UILabel(frame: CGRect(x: 0, y: 0, width: 200, height: 40))
        
        //2. 속성 설정
        nTitle.numberOfLines = 2 //두줄까지 표시되도록 설정
        nTitle.textAlignment = .center//중앙정렬
        nTitle.textColor = UIColor.white // 텍스트 색상 설정
        nTitle.font = UIFont.systemFont(ofSize: 15)//폰트 크기
        nTitle.text = "58개 숙소 \n 1박(1월 10일 ~ 1월 11일)"
        
        //3. 내비게이션 타이틀에 입력
        self.navigationItem.titleView = nTitle
        
        //배경색 설정!
        let color = UIColor(red: 0.02, green: 0.22, blue: 0.49, alpha: 0.8)
        self.navigationController?.navigationBar.barTintColor = color
    }
```

<div>
<img width="300" height="500" src="https://user-images.githubusercontent.com/30828236/54037520-b9bbbd80-4201-11e9-91ee-11d8fa9aae31.png">
</div>
           
#### 내비게이션 타이틀 커스텀 2

```swift
    func initTitleNew(){
        // 1. 복합적인 레이아웃을 구현할 컨테이너 뷰
        let containerView = UIView(frame: CGRect(x: 0, y: 0, width: 200, height: 36))
        
        // 2. 상단 레이블 정의
        let topTitle = UILabel(frame: CGRect(x: 0, y: 0, width: 200, height: 10))
        topTitle.numberOfLines = 1
        topTitle.textAlignment = .center
        topTitle.font = UIFont.systemFont(ofSize: 15)
        topTitle.textColor = UIColor.white
        topTitle.text = "58개 숙소"
        
        // 3. 하단 레이블 정의
        let subTitle = UILabel(frame: CGRect(x: 0, y: 18, width: 200, height: 18))
        subTitle.numberOfLines = 1
        subTitle.textAlignment = .center
        subTitle.font = UIFont.systemFont(ofSize: 12)
        subTitle.textColor = UIColor.white
        subTitle.text = "1박(1월 10일 ~ 1월 11일)"
        
        // 4. 상하단 레이블을 컨테이너 뷰에 추가한다.
        containerView.addSubview(topTitle)
        containerView.addSubview(subTitle)
        
        // 5. 내비게이션 타이틀에 컨테이너 뷰를 대입한다.
        self.navigationItem.titleView = containerView
        
        //배경 색상 설정
        let color = UIColor(red: 0.02, green: 0.22, blue: 0.49, alpha: 0.8)
        self.navigationController?.navigationBar.barTintColor = color
    }
```

<div>
<img width="300" height="500" src="https://user-images.githubusercontent.com/30828236/54037529-baecea80-4201-11e9-85e4-4f494afc55af.png">
</div>

#### 내비게이션 타이틀 3

```swift
func initTitleImage(){
        let image = UIImage(named: "swift_logo")
        let imageV = UIImageView(image: image)
        
        self.navigationItem.titleView = imageV
    }
```
<div>
    <img width="300" height="500" src="https://user-images.githubusercontent.com/30828236/54038227-5a5ead00-4203-11e9-958e-5e7211db2e92.png">
</div>


