# Rust

Rust를 공부하는 공간입니다.  

* nft로그인 
https://github.com/nft-login/nft-login  

3/13 
https://rinthel.github.io/rust-lang-book-ko/ch01-02-hello-world.html

    - 컴파일하기  
    rustc 파일이름.rs  

    - 러스트 매크로  
    println!은 러스트 매크로 (macro).  
    러스트 매크로에 대한 자세한 사항은 부록 D에서 다룰 것입니다.  
    지금은 이 보통의 함수 대신 매크로를 호출하고 있음을 의미한다는 것만 알아두면 됩니다.  


3/14

'Cargo'  
https://rinthel.github.io/rust-lang-book-ko/ch01-03-hello-cargo.html  

Cargo(카고)는 러스트의 빌드 시스템 및 패키지 매니저.  

    - 프로젝트 생성
    $ cargo new hello_cargo --bin

    'cargo를 쓰는 것과 쓰지 않는 것의 차이'
    우리의 이전 프로젝트와 Cargo가 만든 프로젝트 간의 차이점은 Cargo가 코드를 src 디렉토리 안에 위치시킨다는 점,  
    그리고 최상위 디렉토리에 Cargo.toml 환경 파일을 가지게 해준다는 점입니다.  

    - 프로젝트 빌드
    $ cargo build
    hello_cargo 내부에서 실행

    - 프로젝트 실행
    ./target/debug/hello_cargo


    - 프로젝트 빌드 + 실행
    $ cargo run 
    이미 빌드가 되었다면 실행만 함. 수정되었다면 다시 빌드하고 실행함

    - 오류체크
    $ cargo check 
    프로그램을 작성하면서 이것이 컴파일 되는지 확인하기 위해 주기적으로 cargo check을 실행.  
    그런 다음 실행파일을 사용할 준비가 되었을 때 cargo build를 실행합니다.  

    'Cargo의 특징, 장점'
    특징 : 우리 코드가 있는 동일한 디렉토리에 빌드의 결과물이 저장되는 대신, Cargo는 이를 target/debug 디렉토리에 저장합니다.  
    장점 : 
    Cargo를 사용하면 생기는 추가적인 장점은 여러분이 어떠한 운영체제로 작업을 하든 상관없이 커맨드들이 동일하다는 점입니다. 
    따라서 이러한 점 때문에 우리는 더 이상 Linux와 macOS 및 Windows를 위한 특정 명령을 제공하지 않을 것입니다.  


    - 프로젝트 릴리즈(배포)
    $ cargo build --release  

    하나는 여러분이 빠르게 그리고 자주 다시 빌드하기를 원하는 개발용(cargo build), 그리고 다른 하나는  
    반복적으로 다시 빌드를 할 필요 없고 가능한 빠르게 실행되어 여러분이 사용자들에게 제공할 최종 프로그램을 빌드하기 위한 용도입니다.  
    만일 여러분이 코드의 실행 시간을 벤치마킹 중이라면, cargo build --release를 실행하고 target/release의 실행파일을 가지고 밴치마킹하고 있음을 확인하세요.  


