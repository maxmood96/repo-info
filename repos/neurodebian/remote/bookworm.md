## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:1e827b83c9bb8c0bd79408396648f5c4b0a12ad286edffd2eb8f887d836ba1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:0acf4ccd7979f181031416378268c9d195dcd26fcac771e9c385e8ba18b2e905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc12c40eeddd04e825a714126de916daac07b5608eb8c1efd509e1381a6d923d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa63293c58d7f4eb78806fbcdaa17b9c11e011a9808f35f8829dca9a3db4acbf`  
		Last Modified: Tue, 21 Nov 2023 09:04:21 GMT  
		Size: 11.5 MB (11465318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e43a2b83503b547ab65b0ba7ae317f4ed53706435f3c741b606251fd24d8e`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824a0cc551e8a570695ede50032f451cd8096058f66d8ff101a0a5aa3326cd3`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9b428aeb24a379d8cf654d1d67515d70a9de02494ca42e5aaa9ad715df5d1`  
		Last Modified: Tue, 21 Nov 2023 09:04:20 GMT  
		Size: 289.5 KB (289495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:df2635430f6e2aaaa734246f85920cb14bca31aa9bc36e4a99cab72420c965cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61333780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbca19c5aa580fe66fa2b2661edcd2c7e05138e5b3f2282ba3e0b400a0397cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 16:52:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 16:52:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 16:52:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 16:52:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0bb1847f5b7ea227efb55b72c7ea12f7280b47a2394fd973e074f55b56411b`  
		Last Modified: Tue, 21 Nov 2023 16:53:54 GMT  
		Size: 11.4 MB (11429191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2495ed4e628005f7d99eae888e75dae7518f63617cbf3b98ae1258d80ddde082`  
		Last Modified: Tue, 21 Nov 2023 16:53:53 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c63eff6eb61a9f42fa71702a5914b183cfcccb8243da6a925f929ac82261d`  
		Last Modified: Tue, 21 Nov 2023 16:53:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b48f69e2524c0d4dd82bebeb7725dea69728e83ba350033674a6d79b6eabf03`  
		Last Modified: Tue, 21 Nov 2023 16:53:54 GMT  
		Size: 289.9 KB (289927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:f7c4c178c45b68e61a7e60809e3fcdd07f83c4f5a2de2cb91f0735deae72f3b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62778122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbce3d6e257eea0d4d10039c7c1b914c4c3a1bc801a9dcef5f9be5618de87b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:39:42 GMT
ADD file:abe2e7bdcd180971e7231cdda92141480a16075563efb8f61699f50e06bdb708 in / 
# Tue, 21 Nov 2023 04:39:42 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:31:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 14:31:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 14:31:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7a059bd70ecf2a95d7693944fbc8baa8c198f05211b46ff1be263e6bad07b85`  
		Last Modified: Tue, 21 Nov 2023 04:44:08 GMT  
		Size: 50.6 MB (50600840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d141bc88c580d73e2e1667aa5ce675e840d05ff8d5199d47b1fe135f00cccd2`  
		Last Modified: Tue, 21 Nov 2023 14:33:03 GMT  
		Size: 11.9 MB (11885537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdc9c226d38903fdda45c684a29b4d9278094fbcc31a5bdd64c1e66bb8270ea`  
		Last Modified: Tue, 21 Nov 2023 14:33:01 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c37b66b01bef15738065c4d6ac5e93d768abd6f198770627b20d6c5ddd919`  
		Last Modified: Tue, 21 Nov 2023 14:33:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efa2eb36257eed080def30aaaeb3c47e8d155a9067aaed595ce6e812d1de2ac`  
		Last Modified: Tue, 21 Nov 2023 14:33:01 GMT  
		Size: 289.7 KB (289728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
