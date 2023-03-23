## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:32b9f6de5806828b6aac49d44c818109f06a7ba70dbfb55602efeafb3f16f3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:3b6236836430a9b600ad6c23ee170bdab5cb7e8c8f57d92e1c75768e7ddc1b20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61293213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a271e0a7fcc73c4874a05deda7640915a38454a568ef348851239c8350e67185`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:57:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:57:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:57:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:57:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87854b612208107946dc34f8b2c307f8d327dd5e9d9bb230c589e38e39517b7e`  
		Last Modified: Thu, 23 Mar 2023 15:58:44 GMT  
		Size: 11.7 MB (11717776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dd62393e4e67f3515e1db58edc190f05b10d96684fe588165e9439c22b14fe`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e44bc4b8083e27ff5a00477a6d71a509254fa7e50d77b8d41a3c0fc9fd99460`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a35ecff7e273194d23bd146df1031b1d5d40f9ec29f6cefba4f2ba45a67b4`  
		Last Modified: Thu, 23 Mar 2023 15:58:43 GMT  
		Size: 281.8 KB (281792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:24c740bc59d10d0dc004696bc623404ab79f733bec1e1db0e0d6ce7c10066ff3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ca4d0aeba7e98c3dba66e436fb1b58c135a1997e9b831276d8554516354fb5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:31:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:31:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0e8bba10f3b5b2432a2b1218e1c8025aa37e5b2848aba78cb30b14c96d48b`  
		Last Modified: Thu, 23 Mar 2023 09:32:22 GMT  
		Size: 11.7 MB (11677082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c996676719d71c02efc60656700e2212d3ad2c4aad1f607c5baa5644790eaad`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f354b2c84f012c8699569e7416cc07ba57b26ed0f605ae146d61586a3dbc579b`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89a260248440979723f69655c586df9a7be34913dc586e4ccf4a675c842b5d`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 282.2 KB (282220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:416fb65b7df728eee127743ec9ca9882f9d8e082de8c3f447d6d0ea6f2f8c1ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62740204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab2e71590fedf412fb623aa1f27fb45d8055c6a5776495de8c58e65a3c702cb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:40:10 GMT
ADD file:b6719d98d83dc3affc1d45dd9bc533456f19b9fbedf5369cde4c632f24f6146c in / 
# Thu, 23 Mar 2023 00:40:11 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:50:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:50:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 20:50:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 20:50:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dab6ed4b4dcc22cec1b58fa38e2c22941443603bb1cb3a1f4025cca4556556b`  
		Last Modified: Thu, 23 Mar 2023 00:44:54 GMT  
		Size: 50.3 MB (50314549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0a0695c7dd86a7d613032c1b47f7f8f6e5489dcb0fc8291525a9490dd0ae`  
		Last Modified: Thu, 23 Mar 2023 20:51:29 GMT  
		Size: 12.1 MB (12141654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4c4f3b60e69e7c4db38ee990274394e28730f452a263490ece4b510a348f29`  
		Last Modified: Thu, 23 Mar 2023 20:51:28 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1045e421610d0a837c9410230d33924802a152b28a6cc7deb7b390b4f032982`  
		Last Modified: Thu, 23 Mar 2023 20:51:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483566c97a9eb61a7ea75336c517a98c454aa2bc51dc76976d36d47f63fad3bf`  
		Last Modified: Thu, 23 Mar 2023 20:51:28 GMT  
		Size: 282.0 KB (281995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
