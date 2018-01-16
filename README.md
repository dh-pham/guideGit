# guideGit
1. git clean -f: 
    xoá các file chưa git add
    
2. git rebase -i HEAD~n : 
    n là số commit muốn gộp
    gộp n commit lại thành 1 hay 1 số commit. (p -> f)
    
3. git reset --soft HEAD~n : 
    reset trạng thái commit về n commit phía trước
    vẫn giữ nguyên các file code.
    
4. git reset --hard HEAD~n : 
    reset trạng thái cả commit và file code( chỉ file 
đã được commit) về trạng thái n commit trước, các file chưa add vẫn giữ.

7. git revert <commitID>:
    thêm vào ds commit 1 commit mới với mục đích báo hiệu rằng 
    code của mình sẽ trở lại trạng thái commit đó.
    ( khi có người pull phần commit đó về rồi thì không nên reset --hard
    và push -f vì sẽ làm thay đổi lịch sử commit).

5. git checkout -- <tenfile> : 
    đưa file chưa add về trạng thái commit gần nhất.

6. git reset HEAD <tenfile>:
    đưa file đã commit trở lại trạng thái chưa commit ( đã add). 
    
6. git commit --amend : 
    đổi tên commit gần nhất.
    

    
    *) Khi ta thay đổi 1 commit đã được push lên rồi thì sẽ phải push -f.
    *)Chú ý: Force push rất nguy hiểm và chỉ nên được thực hiện khi bạn
    không còn cách nào khác. Nó sẽ viết lại lịch sử commit của app của
    bạn và bạn sẽ mất các bản ghi chép sau bản đang định push.
   
