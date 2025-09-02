## `clojure:temurin-11-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:812ac17f0edf002536ca36dfc3ff5dfc71d153bd69e1b070a4a45566e305cac9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:568dbbcccf8d097a418da6976f8c6d07bbb65b3454ceea869db6093248b60e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280470302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f610f1031c3a60579ff4679aff1e48f33399ec41f372ee90fc0d1513d8bbd2a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3576d5dfba93d945e19d11fe0e9f7b6a236261ee9ea08a6b54ef13ed587ed20`  
		Last Modified: Tue, 02 Sep 2025 00:17:21 GMT  
		Size: 145.7 MB (145658266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8be6a7b744a0a27c1214e987419760b0ee9f01375eff838a8ea31df3ee6b68`  
		Last Modified: Tue, 02 Sep 2025 00:18:06 GMT  
		Size: 85.5 MB (85533110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f3389595214110348ba054106516fdc0bc0dafbbc831d3c9a51434b5c35f09`  
		Last Modified: Tue, 02 Sep 2025 00:17:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bc532fe22598a2a75df97cad4d911d638495a1292ee1ef40d675a76e8aa12f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744024b101f5ffb8f48f39b51a1b85e0a50a311a46c525dc7e30f9cf327363cf`

```dockerfile
```

-	Layers:
	-	`sha256:a9f27e6a0dc92617b0b64f9e077fe4158adb456ac8e3fa2f09247516c9f76f05`  
		Last Modified: Tue, 02 Sep 2025 03:37:26 GMT  
		Size: 7.5 MB (7482362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40807405aeb518ff68cebe0323ff8e255548e29bf17d836ec12191f72b9d7d64`  
		Last Modified: Tue, 02 Sep 2025 03:37:27 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e7a6939d9fcce7a17ea6f470b271ff568a5befaa7d132320bb00fadb1bc4adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277457900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5092305301b839c3b5dcd9e1d64a586af951ccf89a6e5ff1818f58bf17457112`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f306fa734987e66c89f1c46e8533bb72a2daa1ce48f7896df0004c51f6c05bdd`  
		Last Modified: Tue, 02 Sep 2025 07:49:40 GMT  
		Size: 142.5 MB (142459104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8265db3f807a8f7bfc53646c1f893a6e1dcfa22ef1d76ebc28072a10662d00`  
		Last Modified: Tue, 02 Sep 2025 07:56:12 GMT  
		Size: 85.4 MB (85356548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cbe1ff43b0f652b8c0c9b4ba6d4838a23a4fa8a52189915fd60a3ef83438c9`  
		Last Modified: Tue, 02 Sep 2025 07:55:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a3faca2e3ab34f9c95261671292b253f6d5b1e36f71c7983f0bcea11bc05bcc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4922bf183217f02e236b3abd965da1bf9043c6af6bbd7ddd0671ff84e5038884`

```dockerfile
```

-	Layers:
	-	`sha256:21cba77460338f9f116dfd5864432c3ad65afe0f7a6918bcb923999278d36ae8`  
		Last Modified: Tue, 02 Sep 2025 09:37:23 GMT  
		Size: 7.5 MB (7490010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b86905356871f81135bc5a409bd8176fea70c7636418487493ea9cb79d47bfa`  
		Last Modified: Tue, 02 Sep 2025 09:37:23 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:85118b79c68cd8f77085ad52df3e447a9d190c4dc3a5b226d7c1bb26bca10b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276898770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe8740c633c09624cac90cfaf56e02c3767b3117ed5c26e2b751e836889d0d3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d59d569015f70604fe51fcd56c3b07ce6b7dd5197efeeb62cd5cb7f57c9bd69`  
		Last Modified: Tue, 02 Sep 2025 08:16:55 GMT  
		Size: 132.9 MB (132853128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89079b2660190ff7b5a4a123c6bf158ad58739e4ada6275ad2954a10cfd488`  
		Last Modified: Tue, 02 Sep 2025 08:27:02 GMT  
		Size: 90.9 MB (90941611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d543610e3716285b813f4ef7832f0faca80fd553246c46f865268641c0d608`  
		Last Modified: Tue, 02 Sep 2025 09:16:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:25b2caa73e4ba7aeda9a5196d795c9028e08e1a5a6973ec4c49e5fec90ae99e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb1679c8bab73b1061a8848eab9d57b2b0adaede12f9c72726f77a4b0c99c12`

```dockerfile
```

-	Layers:
	-	`sha256:ce479f615a63822e55803ae551895a63b065ced4559ad3f3673bc2c212980f5d`  
		Last Modified: Tue, 02 Sep 2025 09:37:29 GMT  
		Size: 7.5 MB (7486166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d60cc28be9c43f5d3180e02d8ce065257c2ffb4862d50a1aec7f9354efee40a`  
		Last Modified: Tue, 02 Sep 2025 09:37:30 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4e7b44bfe3cf04df130f9e205b20a352a3e0d0ebfb9cce2565c09c3f6c5cc14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261466477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92e71022f867aff35864888662ee5a05f06283e27fe251cdd1e5d983acbb709`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c1a2d3a2f2de1b60ce9f804a69133900188d6f67286a875440572a7d06126f`  
		Last Modified: Tue, 02 Sep 2025 01:48:23 GMT  
		Size: 125.6 MB (125622204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fd7fe2a51113eab35f0202a9c801bf6f0184c2737293a5297ec1af4d674533`  
		Last Modified: Tue, 02 Sep 2025 01:54:50 GMT  
		Size: 86.5 MB (86498466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8462feb0c8e03de1ce83a7c01563316e43caed0f62d93dfe9051c53318bba677`  
		Last Modified: Tue, 02 Sep 2025 01:54:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a7e139c173dc1788b83015b8c241574c257c6fa4aacdc193df4a9cb34519b47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f9b24ef7f9f498c8ae9f948b12f5dd120e7c10a55d45c6e564fbd080c39054`

```dockerfile
```

-	Layers:
	-	`sha256:e91ba588713c8c1a4955f2fea3d8d4ea1d32ae53132a02af3a21569322f94ff2`  
		Last Modified: Tue, 02 Sep 2025 03:37:44 GMT  
		Size: 7.5 MB (7478288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057e6cdd5a614425ae2bfc4bbe13a9485500bc1ed2c8e5cf4651d8bca4f6a8a5`  
		Last Modified: Tue, 02 Sep 2025 03:37:45 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
