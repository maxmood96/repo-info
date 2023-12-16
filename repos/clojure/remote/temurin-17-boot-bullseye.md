## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:90121713f4b3725ab569d63f8857d0c35e7ea2d6b460cece768632e8e145f042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e6b93a314298243263dcf913eb07aed8cf47f16310d323b99d3b97029beb5a50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261121279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bafb045780b96b7ba257a362d5cc8bfaa939c22ca193471baae2e7368117ae2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 15:33:34 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:33:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:33:36 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 15:33:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 15:33:36 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:33:41 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 15:33:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 15:33:42 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 15:33:58 GMT
RUN boot
# Sat, 16 Dec 2023 15:33:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 16 Dec 2023 15:33:59 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Dec 2023 15:33:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244a3c87a460c27f913eb094b158e5637e4f266f77bea10273554345677457cc`  
		Last Modified: Sat, 16 Dec 2023 15:49:26 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c62a7e687237e04eccd07739e7d1f71926fc48f7e8e9c8f71c17c921256d0`  
		Last Modified: Sat, 16 Dec 2023 15:49:16 GMT  
		Size: 2.4 MB (2368729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558c338fa94b1a3f1d512d53e5195684fb438fb002ab92816558d7f70e42493c`  
		Last Modified: Sat, 16 Dec 2023 15:49:18 GMT  
		Size: 58.8 MB (58820349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2757e49ce55001a6e470c3d1cfe46a1c7e8d025fc8fb6888d54d490f14bf4a`  
		Last Modified: Sat, 16 Dec 2023 15:49:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96b9f615939a49622f7a48af797d6fb84b53fad1645dbbcea8de1b5daa40a97a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258568080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b042e559876d120ba5c79f65a14547538830a628f8c510c6dbfafc3bbe55fcc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:53:59 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:54:03 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 08:54:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:54:03 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:54:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 08:54:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:54:08 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 08:54:25 GMT
RUN boot
# Sat, 02 Dec 2023 08:54:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 08:54:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 08:54:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188efff16de26f2786cfb1a16453748b1bec33191f4cc6735aa049a5a316877e`  
		Last Modified: Sat, 02 Dec 2023 09:08:30 GMT  
		Size: 143.7 MB (143681758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1b690d5a045025819d120312ec3a7e63a0fea7a67200648164ed333387fca0`  
		Last Modified: Sat, 02 Dec 2023 09:08:20 GMT  
		Size: 2.4 MB (2357559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053bd9f1246d54ab8f4b8de0fe46768c58902b910fd73e2b3d356389facd28c`  
		Last Modified: Sat, 02 Dec 2023 09:08:23 GMT  
		Size: 58.8 MB (58820490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbab733c6f19ebf129d946f84292df2d5ef92a79d21366af9b148f6f20c3a17d`  
		Last Modified: Sat, 02 Dec 2023 09:08:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
