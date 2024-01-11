## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:2baf5b0172306652b7ce5b5ecab008c8547be1c679e4d52a8532dc951fdcc86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a1fade90941d1299622e238a68b2252c7c1524bf1bd15740dc0906fe33c06522
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261121300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c084b8071897cf27c03c3fb5b7e26f7805d3401646d0b51713ef7849bad8558`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:04:51 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:04:52 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 05:04:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:04:52 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:04:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 05:04:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:04:58 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 05:05:17 GMT
RUN boot
# Thu, 11 Jan 2024 05:05:17 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:05:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:05:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d0fbad402cd2919fb4faf35c70ab5f613bf878017c5eaf98930d965c12791f`  
		Last Modified: Thu, 11 Jan 2024 05:21:53 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56d44e49c6b8cb26e6b011d2c9adf265d0ec91b0dab3f4900f5e16f8a61e9cb`  
		Last Modified: Thu, 11 Jan 2024 05:21:42 GMT  
		Size: 2.4 MB (2368742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2b6fb5a5e33228911f3beeeb846ae6b2b00a33da9e050ebdaea65878a7ace6`  
		Last Modified: Thu, 11 Jan 2024 05:21:45 GMT  
		Size: 58.8 MB (58820531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c2cfe141a739cf84d16f115c7c200bac332a95432aa42cd2b8dd468e40c65`  
		Last Modified: Thu, 11 Jan 2024 05:21:41 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26b85655f9bc8612f4641fdcbfe98cf3735596768735e3c328fad878bad09c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258568074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1943c1add91a6918e4c485e17f9e5d7ce8c306b06fa9e5cdeff20d0be4991e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:55:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:36 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:04:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:04:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:04:39 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:04:44 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:04:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:04:44 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:05:00 GMT
RUN boot
# Tue, 19 Dec 2023 07:05:00 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:05:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:05:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd07311e78c2924fc080a1762e027781ac7b4ae611c86133314aba5a664a33ef`  
		Last Modified: Tue, 19 Dec 2023 07:19:23 GMT  
		Size: 143.7 MB (143681714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0867e5a13d451c249fd405b3af65d25cbffc40503c6a760cb65d45751f4349`  
		Last Modified: Tue, 19 Dec 2023 07:19:14 GMT  
		Size: 2.4 MB (2357517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f97da41410ebd65e975585d05fb49d33bf80f6d668ad0d9813f79e57fbcb94`  
		Last Modified: Tue, 19 Dec 2023 07:19:16 GMT  
		Size: 58.8 MB (58820352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978f694fbd03c66ddeb2afe472f32ccf6d86b8e617735a39b388fb202fd13aca`  
		Last Modified: Tue, 19 Dec 2023 07:19:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
