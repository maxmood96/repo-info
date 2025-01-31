## `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye`

```console
$ docker pull clojure@sha256:c70e02d7f5e7230419ccd3e54898ae8aeed49373a97444877cb41d88c89be8f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0bfc7f33fcfae690ed752f4a739b000933c5828aeff412c2840d86f86532fe7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177651995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a3230e2385b83a2a68abffdd7c090acd00c6a1e60b95d0f11cc39ca14e7f2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c6c5698496fb462d67dc18d9e239d841040d6852ab341c6020e1b1ad3dd33`  
		Last Modified: Fri, 31 Jan 2025 02:14:12 GMT  
		Size: 54.7 MB (54721244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f95d9bc8e935807da7d20462e1e1910a6eaa1dd1ecb50c0c0db9bd1c7cd3339`  
		Last Modified: Fri, 31 Jan 2025 02:14:12 GMT  
		Size: 69.2 MB (69190942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4f68d99ce49025455381599050d6101bb4eefdf40946d0a82c68a77bc384b4`  
		Last Modified: Fri, 31 Jan 2025 02:14:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4ba77a05aa4a58420c65303880d6cb66605538101dbd6cd898be1158e7a91400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fb9d8d4ac5bc16f4746a443b5604c2858c3999a39157175ab18d062fe1bb04`

```dockerfile
```

-	Layers:
	-	`sha256:859f6bbf67a9469f0f8fce302fd8dd647c855a75d0f61f187beae02ad2d6e351`  
		Last Modified: Fri, 31 Jan 2025 02:14:10 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8b4987c69ff02f24be2137191a23833821510b546160145eff96be24921b90`  
		Last Modified: Fri, 31 Jan 2025 02:14:09 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a060db5c994d20c22b4584989be5890cf1d9bfea7fbb2490f30b57e9dbbcef37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175374446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032ece9b0b924453ba6960a46855b2dafba63da4876fb611448a790ee7c3c57f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef99793a2d8bdc381daf53998de5bd5712cc60ecc715ece4034ebadad9db1c4`  
		Last Modified: Thu, 23 Jan 2025 02:26:57 GMT  
		Size: 53.8 MB (53816395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bfe74b559f99ab421d2a8be6b9a47c3603436f22187f99d3720f7b8ce411f4`  
		Last Modified: Wed, 29 Jan 2025 20:39:34 GMT  
		Size: 69.3 MB (69311347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851d094bebe042c0b3c0e9e1c0815d55427ac030e8562f851c751a7c32b9bcc`  
		Last Modified: Wed, 29 Jan 2025 20:39:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1f4a779b6eaac6a04eadd853f6dab436a1a36919201c3528da273dc373b2161a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47acac440d4135fec87c4e67b9cbcf49f045d063d30b55e60b7aed8a39566033`

```dockerfile
```

-	Layers:
	-	`sha256:ffde343c572de610eff5cc84b630205f570380445629b93dd59ce65ac3758c09`  
		Last Modified: Wed, 29 Jan 2025 20:39:32 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac72a3f40286e530899ac02826ec94724b23c7a4e6fa4584253c6ab25cfd1146`  
		Last Modified: Wed, 29 Jan 2025 20:39:32 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json
