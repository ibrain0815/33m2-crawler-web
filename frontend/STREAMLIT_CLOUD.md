# Streamlit Community Cloud 배포 시

- **Python 버전**: 배포 시 **Advanced settings**에서 **Python 3.11**을 선택하세요.  
  (3.13 사용 시 서버 기동 실패로 "Error running app" / "connection refused"가 발생할 수 있습니다.)
- **Main file path**: `frontend/app.py` (또는 저장소 루트 기준 `frontend/app.py`)
- **Secrets**: `BACKEND_URL = "https://배포한-백엔드-URL"` (끝에 `/` 제외)

이미 만든 앱의 Python 버전은 변경할 수 없으므로, 문제가 있으면 앱을 삭제한 뒤 Python 3.11로 새로 배포하세요.
