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
