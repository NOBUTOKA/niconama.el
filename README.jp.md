# niconama.el
Emacs用のニコ生コメントビューア

このパッケージはニコニコ生放送<http://live.nicovideo.jp/>用のコメントビューアです。

このパッケージをrequireし、以下のようにニコニコアカウントを設定してください(ニコニコアカウント以外でのログインには対応していません)

    (setq niconama-user "your@account.com")
    
M-x niconama-comment-viewerで起動し、パスワードを入力し、番組番号をlv付きで入力します。
(パスワードはemacsが起動しているあいだ保持されます。再起動したら再入力が必要です。ファイルへの書き出しはしません。)
C-RET in "Write Comment" buffer submit the contents of this buffer to broadcast.
Write Commentバッファにコメントを書き込み、C-RETで送信します。 

終了するときは、M-x niconama-kill-comment-viewerを使います。コメントビューアの番号を聞かれるので、
コメントビューアバッファのタイトルに<コメントビューア番号>: <放送タイトル>のように表示されているものを入力してください

複数放送の同時視聴にも(一応)対応しています。
また、@コメントやユーザIDからコテハンを取得します。取得したコテハンは、user-emacs-directory(通常は.emacs.d)/kotehan.elに
リストの形で保存されます。
