## `nats:latest`

```console
$ docker pull nats@sha256:f0c80abcc8d86c26b77b4cfbf150821d7e71ace88e2ea39d8a5bfa33caf0317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
