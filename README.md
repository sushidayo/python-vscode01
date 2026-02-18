# python-vscode01

# ファイルを作成して書き込む
with open('hello.txt', 'w') as f:
 f.write("こんにちは\n")
 f.write("エリンです\n")
 f.write("きのこが好きです\n")

# 作ったファイルを読み込んで表示
with open('hello.txt', 'r') as f:
 for r in f:
  print(r.strip())

print("ちなみになんでこんなことをしているかというと、ファイルの読み書きの練習をしているからです。")
print('ちなみにコピペしているだけで、コードの意味は全然分かりません。')

try:
    f = open('foo.txt', 'r')
    for r in f:
        print( r.strip())
    f.close()
except FileNotFoundError:
    print('ファイルが見つかりません')
except Exception as e:
    print(e.args)
    
