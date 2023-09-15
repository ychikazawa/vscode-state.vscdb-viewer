# VS Code state.vscdb Viewer


## Requirement

- [Docker](https://www.docker.com/)
  - docker-compose

## Usage

Build image:

```console
cp docker/python/.env.example docker/python/.env
docker-compose build
```

Add your state.vscdb to source folder.

In Windows, the file is located in `%APPDATA%\Code\User\globalStorage`.

```console
cp <path_to>/state.vscdb source/
```

Run container:

```console
docker-compose up -d
docker-compose exec python bash
```

Go to http://localhost:8888 and you'll see the notebooks.

Run view-state.vscdb.ipynb.

## Memo

state.vscdb can be read by sqlite3.

https://stackoverflow.com/questions/74701706/how-can-i-manually-edit-the-list-of-recently-opened-files-in-vs-code

## Licence

This software is released under the MIT License, see [LICENSE](https://github.com/Haru0517/python-docker-template/blob/master/LICENSE).

## Author

[Yuto Chikazawa](https://github.com/Haru0517)