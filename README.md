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


#### 내비게이션 타이틀 4

```swift
    //텍스트 필드를 이용하여 타이틀을 구성하는 메소드
    func initTitleInput(){
        //텍스트 필드 객체 생성
        let tf = UITextField()
        tf.frame = CGRect(x: 0, y: 0, width: 300, height: 35)
        tf.backgroundColor = UIColor.white
        tf.font = UIFont.systemFont(ofSize: 13)
        tf.autocapitalizationType = .none //자동 대문자 변환 속성사용 off
        tf.autocorrectionType = .no //자동 입력 기능 off
        tf.spellCheckingType = .no // 스펠링 체크 기능 off
        tf.keyboardType = .URL // URL 입력 전용 키보드
        tf.keyboardAppearance = .dark
        tf.layer.borderWidth = 0.3 //테두리 경계선 두께
        tf.layer.borderColor = UIColor(red: 0.60, green: 0.60, blue: 0.60, alpha: 0.8).cgColor
        
        //타이틀 뷰 속성에 대입
        self.navigationItem.titleView = tf
    }
```

<div>
<img width="300" height="500" src="https://user-images.githubusercontent.com/30828236/54038794-bc6be200-4204-11e9-8d0d-92a84c0d96ef.png">
</div>

#### 내비게이션 타이틀 5

```swift
    //텍스트 필드를 이용하여 타이틀을 구성하는 메소드
    func initTitleInput(){
        //텍스트 필드 객체 생성
        let tf = UITextField()
        tf.frame = CGRect(x: 0, y: 0, width: 300, height: 35)
        tf.backgroundColor = UIColor.white
        tf.font = UIFont.systemFont(ofSize: 13)
        tf.autocapitalizationType = .none //자동 대문자 변환 속성사용 off
        tf.autocorrectionType = .no //자동 입력 기능 off
        tf.spellCheckingType = .no // 스펠링 체크 기능 off
        tf.keyboardType = .URL // URL 입력 전용 키보드
        tf.keyboardAppearance = .dark
        tf.layer.borderWidth = 0.3 //테두리 경계선 두께
        tf.layer.borderColor = UIColor(red: 0.60, green: 0.60, blue: 0.60, alpha: 0.8).cgColor
        
        //타이틀 뷰 속성에 대입
        self.navigationItem.titleView = tf
        
        //왼쪽 아이템 영역에 들어갈 뷰
        let back = UIImage(named: "arrow-back")
        let leftItem = UIBarButtonItem(image: back, style: .plain, target: self, action: nil)
        
        //왼쪽 아이템 영역에 이미지 뷰 설정
        self.navigationItem.leftBarButtonItem = leftItem
        
        
        //오른쪽 아이템 영역에 들어갈 컨테이너
        let rv = UIView()
        rv.frame = CGRect(x: 0, y: 0, width: 70, height: 37)
        
        let rItem = UIBarButtonItem(customView: rv)
        self.navigationItem.rightBarButtonItem = rItem
        
        //오른쪽 카운트 값을 표시할 레이블
        let cnt = UILabel()
        cnt.frame = CGRect(x: 10, y: 8, width: 20, height: 20)
        cnt.font = UIFont.boldSystemFont(ofSize: 10)
        cnt.textColor = UIColor(red: 0.60, green: 0.60, blue: 0.60, alpha: 1.0)
        cnt.text = "12"
        cnt.textAlignment = .center
        
        //외곽선
        cnt.layer.cornerRadius = 3 // 모서리 둥글게 처리
        cnt.layer.borderWidth = 2
        cnt.layer.borderColor = UIColor(red: 0.60, green: 0.60, blue: 0.60, alpha: 1.0).cgColor
        
        //레이블을 서브 뷰로 추가
        rv.addSubview(cnt)
        
        //오른쪽 버튼 추가
        let more = UIButton(type: .system)
        more.frame = CGRect(x: 50, y: 10, width: 16, height: 16)
        more.setImage(UIImage(named: "more"), for: .normal)
        
        rv.addSubview(more)
    }

```

<div>
    <img width="300" height="500" src="https://user-images.githubusercontent.com/30828236/54039995-a6abec00-4207-11e9-85fa-9d9542576caa.png">
</div>


