# balabala
import os

def list_files_in_directory(directory_path):
    try:
        # 获取指定目录中的所有文件和文件夹
        items = os.listdir(directory_path)
        
        # 过滤出文件夹中的文件
        files = [item for item in items if os.path.isfile(os.path.join(directory_path, item))]
        
        return files
    except Exception as e:
        print(f"发生错误: {e}")
        return []

# 示例用法
directory_path = '你的文件夹路径'
file_names = list_files_in_directory(directory_path)

print("文件夹中的文件名称:")
for file_name in file_names:
    print(file_name)
