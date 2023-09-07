## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:a7448a17f6c42ed880c14810ee4d09e3466bb4cba447ba25648a23dcac92db39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:41f2d660a750fb1b516b2d47c3b7276df5a2a4d3351f555cd1d9b051abe07759
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c4df626b2634d157a053b87fd936cb792a1feda2d3bf37e5c68c343ffb098d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:39 GMT
ADD file:8415eb847ca46ed1aa1695965af86f1a0f09e8859a7b3c07b2f719404b665102 in / 
# Thu, 07 Sep 2023 00:20:39 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 14:37:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:37:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 14:37:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 14:37:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:38:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:012c0b3e998c1a0c0bedcf712eaaafb188580529dd026a04aa1ce13fdb39e42b`  
		Last Modified: Thu, 07 Sep 2023 00:24:59 GMT  
		Size: 49.6 MB (49557216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd8bedeb7c7c1aa0b895eee3234887fd84cabba1f8c52528270be89a33b268`  
		Last Modified: Thu, 07 Sep 2023 14:39:37 GMT  
		Size: 11.5 MB (11463077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b6a0eb151fa9db9e67d2254fd6c57d09a2d50a9be23b98b61af3343561f80a`  
		Last Modified: Thu, 07 Sep 2023 14:39:36 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de84619c9adc5a54c4dabc2c8fd8c4be3d4392015824e36d195dacb9e6acb489`  
		Last Modified: Thu, 07 Sep 2023 14:39:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640160e20b8abbcc3d8c1c80bd4bf1528b39ff7e853240ae5635b26d60347d09`  
		Last Modified: Thu, 07 Sep 2023 14:39:36 GMT  
		Size: 286.3 KB (286276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935d1d4f562b62160c071e7eb2b48edc90cb682b7afe97101eb4dcce6cdc8f6f`  
		Last Modified: Thu, 07 Sep 2023 14:39:45 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:773e5b6719a2d21daf7e8e28ecce5c574b6408d94bef362caa035fa0dd221080
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15774eca54a2ebea42e493dd818af61a1185a5045c9d90a22bfcfe685343901`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:31 GMT
ADD file:f9dd2b1cc0ba261acd8a3e500c54f6b6e0a46131a32988bfd71cf3c6fc5a7d13 in / 
# Thu, 07 Sep 2023 00:39:32 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:34:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:34:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 09:34:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 09:34:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:34:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:fa34261389f3dee2ecffe9bfe38ae7fd05a1908e98a7486354905aee0f648a6e`  
		Last Modified: Thu, 07 Sep 2023 00:42:39 GMT  
		Size: 49.6 MB (49590783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1416c874d38e794a477cae25f253730bbcbdc5173decc6018f67b0f10b07028b`  
		Last Modified: Thu, 07 Sep 2023 09:35:49 GMT  
		Size: 11.4 MB (11426925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cff783984c16c1d2c63bb7a880692867213838e5db34a585a3d4a74463067e`  
		Last Modified: Thu, 07 Sep 2023 09:35:47 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6517bd8408f9f2a2f6a4a782b8acc937a0a751873d9ed96f60bbd261688d73d7`  
		Last Modified: Thu, 07 Sep 2023 09:35:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dc72df4937212f4c5bf4361e27182ead34548335baa997db0f5d05e78f2541`  
		Last Modified: Thu, 07 Sep 2023 09:35:47 GMT  
		Size: 286.6 KB (286590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6577a2d1637c847536e96f40d14cd14968609b1f41a211d8915e5c0e10e79ba3`  
		Last Modified: Thu, 07 Sep 2023 09:35:58 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:526dcaac027b9f279a091b84c5229f820a6e559394bba34a016cf20f35b0c90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62739422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d40c3b46451157027510b0a4c62e6ce22e5d8d9b0242c27865c14691ac0c35`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:38:49 GMT
ADD file:8f184a190a3b39f8a44c9c20af46dd27ea11f07138459893b113592302f90a40 in / 
# Thu, 07 Sep 2023 00:38:50 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:06:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:06:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 01:06:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 01:06:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:06:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:28e9e767fc740145a9fd9e593c7ed9b1ab1ed746324049bf58752d28fa197e5d`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 50.6 MB (50567259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126f8178f039dcde5b94c5baf1f416aed99bd468dddfef648d7076666f7cbb4f`  
		Last Modified: Thu, 07 Sep 2023 01:08:06 GMT  
		Size: 11.9 MB (11883296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1356286a96b0846f065e50ae2b83533053e39cea782cfec01197c95320634581`  
		Last Modified: Thu, 07 Sep 2023 01:08:04 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a9b23cb2c8f0fbdae7c23049e3870d5aaf7ae1f8a9693ec423335f0649d926`  
		Last Modified: Thu, 07 Sep 2023 01:08:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdb8aed3103dc8c360d23a2a95b6a20a7ff20bcbf4fac20b81e7ca8e397ba89`  
		Last Modified: Thu, 07 Sep 2023 01:08:04 GMT  
		Size: 286.4 KB (286420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4788427001dfec518f77344ce0e4c02fad03f95117a36d2e723399e493f6dda`  
		Last Modified: Thu, 07 Sep 2023 01:08:14 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
