## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:68ddbf075dfb8e37bf8a0583d40d1c184164a9858e18b8e7acca39c4370fbdcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dc7d6d29771eaf2e0f32a51aa6c0cbd42a81d03083dd2bfc54e20f6f8cc40af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217508163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac70d8f4e1f171af110623b9862b02ccf678d64985cb9ae19f3e35f097281e1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:51:42 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:51:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:51:43 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:51:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:51:43 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:51:50 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:51:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:51:50 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:52:40 GMT
RUN boot
# Thu, 11 Jan 2024 04:52:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ee0cab5ab6aa98c37ed3fc43d77bcaf83ea4c8a69ec6d510ecb9e0057ee49c`  
		Last Modified: Thu, 11 Jan 2024 05:14:21 GMT  
		Size: 103.6 MB (103598285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbad9ae50351bc0224317832f3ce474c72568b5010ee6bb51a05277c0d8834f`  
		Last Modified: Thu, 11 Jan 2024 05:14:12 GMT  
		Size: 5.5 MB (5527108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b6d6edcd5baea68eafe2adb0ad97f551010088a5ce1668f28119d93e309030`  
		Last Modified: Thu, 11 Jan 2024 05:14:14 GMT  
		Size: 58.8 MB (58821280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:745ce9f058ea66390c32fd7a2cea050f24e6093d903fa4a11cd33301897c19a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216463593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c0084b7c5c2a0686c6ef5b6fc1e0c1903fe941c8aae5e8a51d6f9160baa3d6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:54:25 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:54:27 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:54:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:54:27 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:54:32 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:54:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:54:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:54:49 GMT
RUN boot
# Tue, 19 Dec 2023 06:54:49 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd83395931034d8cc43b9c1210837008aa4d9f602c045c8c2f80b89be5b9e2`  
		Last Modified: Tue, 19 Dec 2023 07:12:44 GMT  
		Size: 102.7 MB (102701533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486bc581fec8cf9127552a0c670f1ade77753be94ce3bd64fb33bc5008643c81`  
		Last Modified: Tue, 19 Dec 2023 07:12:38 GMT  
		Size: 5.3 MB (5349257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d269201e4fa5e82b9626b17ee530a54a968b9b4fd18f5f57cbc2aeb948898464`  
		Last Modified: Tue, 19 Dec 2023 07:12:41 GMT  
		Size: 58.8 MB (58820544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
