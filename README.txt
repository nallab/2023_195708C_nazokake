/content/drive/MyDrive/実験/learn_data/ -- original_double.txt　MASKのない謎かけテキストファイル
																|--Double_MASk.txt　MASKが二つついてる謎かけテキストファイル
																|--SINGLE_MASK_AFTER.txt　MASKが一つついてる謎かけテキストファイル
																
パターンAを実行すると
/content/drive/MyDrive/実験/result/パターンA/ --- train_loss.txt　trainデータに対するloss
																		    |- val_loss.txt　検証データに対するloss
													 						|- テストデータ -- epoch1 --- test_score　予測精度
													 												  				   |- test_predict　予測結果
													 												  --epoch2 ---　epoch1と同じ構造
													 												  			・
													 												  			・
													 												  --epochX--- Xは回したエポック数
																			|- 検証データ -- 　テストデータと同じ構造
																			|- 訓練データ -- 　テストデータと同じ構造
のファイル構造ができ、パターンAの結果が保存される。
パターンBを実行するとパターンAのファイルと追加で以下の「全助詞データ」がある。
/content/drive/MyDrive/実験/result/パターンB/全助詞データ/  -- epoch1 --- test_score　予測精度
													 											  |				   |- test_predict　予測結果
													 											  |--epoch2 ---　epoch1と同じ構造
													 											  |  			・
													 											  | 			    ・
													 										      |--epochX--- Xは回したエポック数

その後、GPTスコア算出の実行により、パターンBで予測した結果のスコアの算出をする。		