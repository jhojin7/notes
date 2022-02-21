---
planned: 16-18
covered: 16-18
---
# ablestudy 2022-02-21
- 실습할때 강사님이 사용하는 데이터: https://www.data.go.kr/data/15058578/openapi.do
	- 데이터셋 설명 페이지(맨밑에 샘플코드 있음): https://www.data.go.kr/tcs/dss/selectApiDataDetailView.do?publicDataPk=15058578
	- 신청 후 승인은 안 기다리고 바로 나서 활용 가능했음.
- 사이트에서 샘플 request 해봤는데, http로 리퀘스트 보내서 크롬이 거름. 
- Sample request url: 
```
http://apis.data.go.kr/B552061/jaywalking/getRestJaywalking
?serviceKey=_____
&searchYearCd=2015 &siDo=11 &guGun=320
&type=json &numOfRows=10 &pageNo=1
```

## Eclipse 설치
- 이클립스 설치해봤는데 강의랑 안맞는거 잘못 설치한듯함. 
	- 인스톨러 에서 "Eclipse IDE for Java Developers" 설치했었음.
	- 그래서 인스톨러에서 "Eclipse IDE for Enterprise Java and Web Developers"를 설치하니까 (강의에서 처럼은 아니지만) 우클릭->New->Others에 Dynamic Web Project 있긴했음.
- 결론: eclipse 사용법이나 자바를 다루는 법을 몰라서 일단 설치만 해두고 repl 쓰는중. ~~자바는 역시 손에 안익는다...~~

- API request걸어서 정보 얻어오는 법 요약 (다른 언어들도 비슷한 흐름?)
	- request 할 url 조합하기. (request parameter 합치기): `GET`
	- url로 연결 만들고, request method, requst proprty명시: `Content-type...`
	- response 받기
	
## 나중에 찾아볼 거
- HttpURLConnection
- bufferedReader, writer
	- 입출력 관련 클래스.
	- 왜 백준이 연관검색어로 뜨는거지?
- InputStreamReader

## Code
```java
// imports
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.HttpURLConnection;
import java.net.URL;

class Main {
  public static void main(String[] args) {
    System.out.println("Hello world!");

    // input buffer
    BufferedReader br = null;
    try{
        // API url
        String urlStr = "REQUEST URL";

        // REST GET request
        URL url = new URL(urlStr);
        HttpURLConnection urlConn = (HttpURLConnection) url.openConnection();
        urlConn.setRequestMethod("GET"); 
        urlConn.setRequestProperty("Content-type", "application/json");
        // urlConn = GET response // 200 OK
        System.out.println("Response Code: " + urlConn.getResponseCode() + " " + urlConn.getResponseMessage());
        
        // read response json into stdin using BufferedReader
        br = new BufferedReader(new InputStreamReader(urlConn.getInputStream(),"UTF-8"));
        
        //*//
        String rst = ""; // readstring
        String line;
        while ((line = br.readLine())!= null){
            rst += line + "\n";
        }
        System.out.println(rst);
		
        /*/
        StringBuilder sb = new StringBuilder();
        String line; // stringbuilder
        while ((line = br.readLine())!= null){
            sb.append(line);
        }
        System.out.println(sb);
        //*/

        // close BufferedReader
        br.close();
        // disconnect request
        urlConn.disconnect();
    }
	// exception handling
    catch (Exception e){
        System.out.println(e.getMessage());
    }
  }
}
```

## Resources
- BufferReader, Writer
	- https://machine-geon.tistory.com/79
	- https://codechacha.com/ko/java-bufferedreader-bufferedwriter/
	- https://jhnyang.tistory.com/m/92
- URLConnection
	- https://derveljunit.tistory.com/155
- HttpURLConnection
	- https://ju-hy.tistory.com/65