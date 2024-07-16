import os
import jsbeautifier
import autopep8
from bs4 import BeautifulSoup
import cssbeautifier

BEAUTIFY_FUNCTIONS = {
    '.js': jsbeautifier.beautify,
    '.php': autopep8.fix_code,
    '.html': lambda content: BeautifulSoup(content, 'html.parser').prettify(),
    '.css': cssbeautifier.beautify
}

file_counts = {'.html': 0, '.css': 0, '.js': 0, '.php': 0}

def beautify_file(file_path):
    _, ext = os.path.splitext(file_path)
    if ext in BEAUTIFY_FUNCTIONS:
        with open(file_path, 'r', encoding='utf-8') as file:
            content = file.read()
        beautified_content = BEAUTIFY_FUNCTIONS[ext](content)
        with open(file_path, 'w', encoding='utf-8') as file:
            file.write(beautified_content)
        file_counts[ext] += 1

def beautify_directory(directory):
    for root, _, files in os.walk(directory):
        for file in files:
            file_path = os.path.join(root, file)
            beautify_file(file_path)

directory_path = r'your_directory_path'
beautify_directory(directory_path)

for ext, count in file_counts.items():
    print(f'{count} {ext} files beautified')
