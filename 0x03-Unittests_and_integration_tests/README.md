# 0x03-Unittests_and_integration_tests
The project is focused on learning and practicing unit testing and integration testing in Python. It involves creating tests for various functions and methods to ensure their correctness and reliability. The tests cover different aspects of testing, such as parameterization, mocking HTTP calls, using decorators, and handling integration tests with fixtures. The overall goal is to gain proficiency in writing comprehensive tests to validate code functionality, handle edge cases, and ensure robustness in Python applications.
### project Details in short form

| Task ID | Task Name | Description |
|---------|------------|-------------|
| 0 | Parameterize a unit test | Write the first unit test for `utils.access_nested_map`, using `@parameterized.expand` to test multiple inputs. |
| 1 | Parameterize a unit test with exceptions | Implement `TestAccessNestedMap.test_access_nested_map_exception` to test that `utils.access_nested_map` raises `KeyError` for certain inputs. |
| 2 | Mock HTTP calls | Implement `TestGetJson.test_get_json` to test `utils.get_json` using `unittest.mock.patch` to mock external HTTP calls. |
| 3 | Parameterize and patch | Implement `TestMemoize.test_memoize` to test `utils.memoize` decorator, ensuring a method is called only once. |
| 4 | Parameterize and patch as decorators | Implement `test_org` method in `TestGithubOrgClient` class to test `GithubOrgClient.org` using `@patch` and `@parameterized.expand`. |
| 5 | Mocking a property | Implement `test_public_repos_url` to unit-test `GithubOrgClient._public_repos_url` by mocking `GithubOrgClient.org`. |
| 6 | More patching | Implement `TestGithubOrgClient.test_public_repos` to unit-test `GithubOrgClient.public_repos` by mocking `get_json` and `_public_repos_url`. |
| 7 | Parameterize `has_license` | Implement `TestGithubOrgClient.test_has_license` to unit-test `GithubOrgClient.has_license` using parameterized inputs. |
| 8 | Integration test: fixtures | Implement `TestIntegrationGithubOrgClient` class to test `GithubOrgClient.public_repos` using fixtures and mocking `requests.get`. |
| 9 | Integration tests | Implement `test_public_repos` and `test_public_repos_with_license` to test `GithubOrgClient.public_repos` using integration tests and fixtures. |

### Detailed Task Descriptions

#### Task 0: Parameterize a unit test
- **Objective**: Write a unit test for the `utils.access_nested_map` function.
- **Requirements**:
  - Create a `TestAccessNestedMap` class.
  - Implement `TestAccessNestedMap.test_access_nested_map` method.
  - Use `@parameterized.expand` to test multiple inputs.
  - Verify function output with `assertEqual`.

#### Task 1: Parameterize a unit test with exceptions
- **Objective**: Write a unit test to ensure `utils.access_nested_map` raises `KeyError` for invalid inputs.
- **Requirements**:
  - Implement `TestAccessNestedMap.test_access_nested_map_exception`.
  - Use `assertRaises` to check for `KeyError`.
  - Parameterize the test with invalid inputs using `@parameterized.expand`.
  - Verify exception messages.

#### Task 2: Mock HTTP calls
- **Objective**: Test `utils.get_json` without making actual HTTP calls.
- **Requirements**:
  - Define `TestGetJson` class.
  - Implement `TestGetJson.test_get_json` method.
  - Use `unittest.mock.patch` to mock `requests.get`.
  - Verify the function's behavior with mocked HTTP responses.
  - Ensure the mocked `get` method is called once per input.
  - Compare function output to expected payloads.

#### Task 3: Parameterize and patch
- **Objective**: Test the `utils.memoize` decorator.
- **Requirements**:
  - Implement `TestMemoize` class.
  - Define an inner `TestClass` with `a_method` and `a_property`.
  - Use `unittest.mock.patch` to mock `a_method`.
  - Verify `a_property` calls `a_method` only once.

#### Task 4: Parameterize and patch as decorators
- **Objective**: Test `GithubOrgClient.org` method.
- **Requirements**:
  - Declare `TestGithubOrgClient` class.
  - Implement `test_org` method.
  - Use `@patch` to mock `get_json`.
  - Use `@parameterized.expand` to test multiple org inputs.
  - Ensure no external HTTP calls are made.

#### Task 5: Mocking a property
- **Objective**: Test `GithubOrgClient._public_repos_url` property.
- **Requirements**:
  - Implement `test_public_repos_url`.
  - Use `patch` to mock `GithubOrgClient.org`.
  - Verify `_public_repos_url` returns expected results based on mocked payload.

#### Task 6: More patching
- **Objective**: Test `GithubOrgClient.public_repos` method.
- **Requirements**:
  - Implement `TestGithubOrgClient.test_public_repos`.
  - Use `@patch` to mock `get_json`.
  - Use `patch` to mock `_public_repos_url`.
  - Verify the list of repos and ensure mocked methods are called once.

#### Task 7: Parameterize `has_license`
- **Objective**: Test `GithubOrgClient.has_license` method.
- **Requirements**:
  - Implement `TestGithubOrgClient.test_has_license`.
  - Use `@parameterized.expand` to test multiple repo and license_key inputs.
  - Verify function output matches expected values.

#### Task 8: Integration test: fixtures
- **Objective**: Perform integration tests on `GithubOrgClient.public_repos`.
- **Requirements**:
  - Implement `TestIntegrationGithubOrgClient` class.
  - Use `setUpClass` and `tearDownClass` methods.
  - Use `@parameterized_class` to apply fixtures.
  - Mock `requests.get` with appropriate payloads using `side_effect`.

#### Task 9: Integration tests
- **Objective**: Further integration tests on `GithubOrgClient.public_repos`.
- **Requirements**:
  - Implement `test_public_repos` and `test_public_repos_with_license`.
  - Ensure method returns expected results based on fixtures.
