# tes_repo
test_repo
---
```
check-mockery:
	@current_version=$$(mockery -version); \
	if [[ -z "$$current_version" || "$$current_version" < "2.43.0" ]]; then \
		echo "Mockery is not installed or version is less than 2.43.0. Installing latest version..."; \
		go get github.com/vektra/mockery/v2/... && go install github.com/vektra/mockery/v2/cmd/mockery@latest; \
	else \
		echo "Mockery version $$current_version is up to date."; \
	fi
```
