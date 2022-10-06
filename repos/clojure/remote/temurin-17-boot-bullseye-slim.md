## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:5908dbbfc8e48b3418d46aa8a69c94a506197963390d288768c86a3500845dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a38d72c2320bf7ce898fa1941b4a6e63fba196529f93ac6a333b7f2b9e3bc003
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283456053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536b5ab9fa3b88a06f1764c2ea5bdc0f5baad2c81a88aa01b9941e25d6d759a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:56:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:56:42 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 03:56:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:56:42 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:56:48 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 03:56:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:56:48 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 03:57:07 GMT
RUN boot
# Thu, 06 Oct 2022 03:57:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 03:57:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 03:57:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31f1d6a7f714c2bcc58ec0f3ed4f72c564669062469e52124a17db014025c71`  
		Last Modified: Thu, 06 Oct 2022 04:12:19 GMT  
		Size: 1.1 MB (1077333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffef3c5833ffeb12744e747b804419e19dfa6331770fb778535e84d25bd75f`  
		Last Modified: Thu, 06 Oct 2022 04:12:22 GMT  
		Size: 58.8 MB (58820594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2c1c974b9488ae41bf0b5d6b8d7abf41e9eefe1fc9fc28b6460ec68a2db2e5`  
		Last Modified: Thu, 06 Oct 2022 04:12:18 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6257eddeee72929bf6464a29a0efdac5fa783b12e280b1bdbc3fb00aa55da57f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280644330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36706d3eeed93a063669034a56dcb0f39ad32288c80b9fe959f071adc2a52c33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:39:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:39:48 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:39:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:39:50 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:39:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:39:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:39:58 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:40:13 GMT
RUN boot
# Thu, 06 Oct 2022 02:40:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:40:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:40:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3dc1ff9fe9090bfcd1bf503b2798ef1e1ea3dc429e1a3b8095249e5a30705`  
		Last Modified: Thu, 06 Oct 2022 03:01:21 GMT  
		Size: 859.3 KB (859259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e9f090ba7587285084eb58bc5e2db02fd4c9c536d98eed40a1cfd964cabc3e`  
		Last Modified: Thu, 06 Oct 2022 03:01:25 GMT  
		Size: 58.8 MB (58816036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220f891db70aa9b7089d64feea5ed49279de1c6acf5d799d985421c96b229d5b`  
		Last Modified: Thu, 06 Oct 2022 03:01:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
