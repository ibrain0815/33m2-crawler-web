# Streamlit Community Cloud 배포 시

- **Python 버전**: 배포 시 **Advanced settings**에서 **Python 3.11**을 선택하세요.  
  (3.13 사용 시 서버 기동 실패로 "Error running app" / "connection refused"가 발생할 수 있습니다.)
- **Main file path**: `frontend/app.py` (또는 `frontend/app_minimal.py`로 먼저 테스트)
- **Secrets**: `BACKEND_URL = "https://배포한-백엔드-URL"` (끝에 `/` 제외)

**connection refused가 계속될 때:**  
1. 앱을 **삭제**한 뒤, **Python 3.11**로 **새 앱**을 만드세요. (기존 앱의 Python 버전은 변경 불가.)  
2. 먼저 **Main file path**를 `frontend/app_minimal.py`로 두고 배포해 보세요. "Hello"가 보이면 Cloud는 정상이고, 메인 앱(`app.py`) 쪽 원인입니다. 그다음 다시 `frontend/app.py`로 바꿔 배포하면 됩니다.
