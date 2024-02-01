## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:3815108720f2ca3ea16182ccd0de0044850ba48d336cae6986dd6d750b15a488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b26ea5721baf2f7f9580921d43ea820da55be41a7577039696d5e0c48338c964
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49141086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9276097ad61fac8508eb9cdd965fd4fddd53f4ea8e69774ed0234be6fd33c9e7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:23:17 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:23:19 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 01 Feb 2024 06:23:19 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Thu, 01 Feb 2024 06:23:24 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:23:24 GMT
VOLUME [/data]
# Thu, 01 Feb 2024 06:23:24 GMT
WORKDIR /data
# Thu, 01 Feb 2024 06:23:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 01 Feb 2024 06:23:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9f2741f102a5fb3dfbb07be2a7a733970ff936b0a0ecb13be0aa60c5c2a4f0`  
		Last Modified: Thu, 01 Feb 2024 06:23:37 GMT  
		Size: 9.8 MB (9789311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f702a8a0965483f91df41faa5d7df04f2e06311cd37f66a1015681a0b65ca`  
		Last Modified: Thu, 01 Feb 2024 06:23:36 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d567baee39489f9e2aa2804a9600ae917e627899c28eb4a5c1c4952ea6d39c13`  
		Last Modified: Thu, 01 Feb 2024 06:23:37 GMT  
		Size: 10.2 MB (10198496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f3dad2b14b2b05ff698b1b79dcdc41025e4e4f52fa15f1b95df1006d67c65c`  
		Last Modified: Thu, 01 Feb 2024 06:23:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:ed24662b3969ae921c43b7170b8de8d4e5fe500b834b25062d08b2a8275baa88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48338447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc518e60e493dcd7bc15ce3b29f628f19eac5b50cc1f0b27c97168213566d67`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:55:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:55:54 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 01 Feb 2024 05:55:54 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Thu, 01 Feb 2024 05:55:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:55:58 GMT
VOLUME [/data]
# Thu, 01 Feb 2024 05:55:58 GMT
WORKDIR /data
# Thu, 01 Feb 2024 05:55:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 01 Feb 2024 05:55:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ffbb7902f4239276a076ba387148c4ce82eb7683807a2fbba052e28066a4`  
		Last Modified: Thu, 01 Feb 2024 05:56:10 GMT  
		Size: 9.6 MB (9586176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc1b0fb9f7312e279e674b2dfbae33e2ced36c50ac988b8bd2cce30e783c1a7`  
		Last Modified: Thu, 01 Feb 2024 05:56:09 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f069352783c1133f713bc627b5a920bb9d7177ced3aaef00cda22849d6d3d7f`  
		Last Modified: Thu, 01 Feb 2024 05:56:10 GMT  
		Size: 9.6 MB (9568628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e4e979e047a587782f00d285e53cf9859a3ee98ff8b892e776785cc84767c`  
		Last Modified: Thu, 01 Feb 2024 05:56:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:68127a0ba51fe15382bd396e5ce609d7a158f78d066b07c3054e1e22c2c632bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4711c8d363678172361e491d04ee0aaae0245cbbb625de3ed63f6615a46ed57`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 31 Jan 2024 22:58:51 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 31 Jan 2024 22:58:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:48:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:48:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 01 Feb 2024 05:48:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Thu, 01 Feb 2024 05:49:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:49:03 GMT
VOLUME [/data]
# Thu, 01 Feb 2024 05:49:03 GMT
WORKDIR /data
# Thu, 01 Feb 2024 05:49:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 01 Feb 2024 05:49:03 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb5adff9476e5554e0ddfe099dd99f85b79016d376c43410faa033fa8a91789`  
		Last Modified: Thu, 01 Feb 2024 05:50:16 GMT  
		Size: 9.3 MB (9285130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fc8294d4fc922f209072451c95ba642f18dc645463937874c828fa7a9b7a8d`  
		Last Modified: Thu, 01 Feb 2024 05:50:15 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f90c30b1c3c02591195ea1bc06347be532b56144b6c09b353bb4162d6d1b71e`  
		Last Modified: Thu, 01 Feb 2024 05:50:16 GMT  
		Size: 9.5 MB (9509408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee105e184991ce3b64da6db6e4a4687a76d688c04acbb19ae2b4944082c5f031`  
		Last Modified: Thu, 01 Feb 2024 05:50:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
