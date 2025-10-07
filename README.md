on:
  push:

jobs:
  test:
    runs-on: windows-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.x'

      - name: Run script
        run: python PyTest.py
