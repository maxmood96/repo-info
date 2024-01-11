## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:f7a89f4059b6183feb91d3115784da1174328f761e1630d4cea9fc5ef78753bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

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

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2c65ead0c831f86d6c40b568b15b547e921fe7044d5f5f0f0ee8d00ed074ef4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258567679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb0dbf1815f2a6f9e084ded4d8d09941f103f5751e1cd0f0e1537be0a7c36fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 08:09:55 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 08:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:09:59 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 08:09:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 08:09:59 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 08:10:03 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 08:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 08:10:04 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 08:10:20 GMT
RUN boot
# Thu, 11 Jan 2024 08:10:20 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 08:10:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 08:10:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f7778a4aa613529fc760536aff987370ee5d52c6e2dd39ce6376024d1b214`  
		Last Modified: Thu, 11 Jan 2024 08:24:37 GMT  
		Size: 143.7 MB (143681700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c788203b675320c65f53c1a2ac321d86a83e73c8ac760b7ec10ce87bb70dfc3`  
		Last Modified: Thu, 11 Jan 2024 08:24:28 GMT  
		Size: 2.4 MB (2357329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22755a56af1fd67de62266f8db899cb75a0c2e5b1884a6816afb9c87c9f928fc`  
		Last Modified: Thu, 11 Jan 2024 08:24:31 GMT  
		Size: 58.8 MB (58820405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c212884d5193cf95fdaed922f3ffc424673a9bebca6ff497050c9531b8a6b751`  
		Last Modified: Thu, 11 Jan 2024 08:24:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
