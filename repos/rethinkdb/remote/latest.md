## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:2c4060355a3f44f138119f8628fea45a9db04ec0cd02c56ba561442210ba4243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:0bf8d6619dcbc239816dbe497355673e1ab69c8558129c4b3769d65a3ea32cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47985799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c607dad87fee8a50ec103ece265f1abe2262f5a031476038fd719f9ed6e316f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:34:16 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:34:18 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 12 Apr 2023 07:34:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 12 Apr 2023 07:34:24 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:34:24 GMT
VOLUME [/data]
# Wed, 12 Apr 2023 07:34:24 GMT
WORKDIR /data
# Wed, 12 Apr 2023 07:34:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 12 Apr 2023 07:34:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fca1159d1d210a4d04b91ebd2339f85210df48bce91c92cf706163be10f593`  
		Last Modified: Wed, 12 Apr 2023 07:34:35 GMT  
		Size: 6.3 MB (6328851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243e62ee81fba2adf5794202f7e0ed35c60ee0956937768b333cd5cd5f821f46`  
		Last Modified: Wed, 12 Apr 2023 07:34:34 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e45aa5e249fcd3109b529ee19a2e1a2a33e4f00253d8a68dc96ee3d54204b`  
		Last Modified: Wed, 12 Apr 2023 07:34:35 GMT  
		Size: 10.2 MB (10235909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add10369539f54c5d656d75bd363b7642ee695d81aa26c3163c95cd14789aeb1`  
		Last Modified: Wed, 12 Apr 2023 07:34:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:97c4230d08ac9fbc3c031f8c810bb828d5731b2a2de2a8ad346e9e93044803b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45953137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fac1ae9fdc6e9d61a8c6f66c9c10479dcd514ffb6d17a96e734035e025364e3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:30:26 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:30:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 03 May 2023 18:30:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 03 May 2023 18:30:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:30:32 GMT
VOLUME [/data]
# Wed, 03 May 2023 18:30:32 GMT
WORKDIR /data
# Wed, 03 May 2023 18:30:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 03 May 2023 18:30:32 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb078617881c650879ddd46eb3cdfa91e38c015026cd670783804933b9de21de`  
		Last Modified: Wed, 03 May 2023 18:30:43 GMT  
		Size: 6.3 MB (6309708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef258d4f30af2b602534072b604720e411c306912e753a8ae672346eb66ed12b`  
		Last Modified: Wed, 03 May 2023 18:30:42 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3b03236fb9f50e7e68164242219ba1a1859d2531433e1363b4e3f77dbabe64`  
		Last Modified: Wed, 03 May 2023 18:30:43 GMT  
		Size: 9.6 MB (9587881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb111c99c796eb1f6a4107e16365e95055bead8c42f47bb96b51aa69667ad068`  
		Last Modified: Wed, 03 May 2023 18:30:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:778ac6330ad7fc9bf3ef5846216c5992699fae1d5767ea1da703d9841ae4c180
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45434192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b14e9de338ca01be7c395859a869e4d713e739796fb45f1597d9080434b4bf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:00 GMT
ADD file:b6463dba97ba9c0a29bacfafc4d67bc603ab57e80b75e23cd42d7ef4b0f8e6ae in / 
# Wed, 12 Apr 2023 00:01:04 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:12:47 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:12:50 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 12 Apr 2023 07:12:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 12 Apr 2023 07:12:55 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:12:55 GMT
VOLUME [/data]
# Wed, 12 Apr 2023 07:12:55 GMT
WORKDIR /data
# Wed, 12 Apr 2023 07:12:55 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 12 Apr 2023 07:12:55 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:97fe10bc7def58e7938e97e41eec4788ec7a45b6ef2cb1770cec02fa831fd19d`  
		Last Modified: Wed, 12 Apr 2023 00:05:18 GMT  
		Size: 29.7 MB (29653156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a487ebc022ead014edc6c256db4b1b870e3c40b460569bb74f1272d3b720a5`  
		Last Modified: Wed, 12 Apr 2023 07:13:09 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e9bd6d603a4d2ede8f4152c4864c47ff98a170c7742163230d8dd812f6e8b6`  
		Last Modified: Wed, 12 Apr 2023 07:13:08 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea8f8e8ab1fdccd4ee306bec44bdccb18c9345634f75ffd65c56d3bacd78aeb`  
		Last Modified: Wed, 12 Apr 2023 07:13:10 GMT  
		Size: 9.6 MB (9572534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1af7a03773b3f6705dc831d1df1b64d81502c630c25b321e43400f36414bec`  
		Last Modified: Wed, 12 Apr 2023 07:13:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
