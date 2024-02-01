## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:e7dede07fa7029251c608143280a6702af80844d070bf0c7627447950fb55137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a1d5c7aae48eb73159010407864b2a0cdd831b556d103f72acd76986d0aee46f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194909655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89394b7207b2b8360899a29b8c4ad83cef949492234d800d6a9c056b153501d3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:44:36 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:44:37 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:44:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:44:37 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:44:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:44:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:44:42 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:45:02 GMT
RUN boot
# Wed, 31 Jan 2024 23:45:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f1c7bfdaddc71e83c67b85b893fc8356c320085ad7fd07d8155f9936128564`  
		Last Modified: Thu, 01 Feb 2024 00:06:04 GMT  
		Size: 103.6 MB (103591889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d94d1e922b6270e9142d3637660872c8fd85701a03c68957add4f38f6eb650d`  
		Last Modified: Thu, 01 Feb 2024 00:05:56 GMT  
		Size: 1.1 MB (1079453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a131cfac0c5f903f871c34b93b6a7f9ea331f090771a9824af28bf16bde331ca`  
		Last Modified: Thu, 01 Feb 2024 00:06:00 GMT  
		Size: 58.8 MB (58820486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71bb7837137597cfc099c8663d43622e8502ff25015b5d1ab3cad7bf0052ef80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192654779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09cb7431dd7cff3d56a005cee85dcc74cf3d30815822a503c552774b11f20a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:21:13 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:21:16 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:21:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:21:16 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:21:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:21:21 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:21:39 GMT
RUN boot
# Thu, 01 Feb 2024 06:21:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e843c549a84c35b323e6c68534d42548cf20689935e9bb3e3ddcddf0dc445f8`  
		Last Modified: Thu, 01 Feb 2024 06:39:51 GMT  
		Size: 102.7 MB (102703026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051d2b83579d409f5e68eb78d8959f897b026b9985e942f7a53dcdd635a430e`  
		Last Modified: Thu, 01 Feb 2024 06:39:44 GMT  
		Size: 1.1 MB (1066899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f823ef311815829cdcc5dfa98df8fdab9561b7834ba2fff530e4363724f87b`  
		Last Modified: Thu, 01 Feb 2024 06:39:47 GMT  
		Size: 58.8 MB (58820520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
