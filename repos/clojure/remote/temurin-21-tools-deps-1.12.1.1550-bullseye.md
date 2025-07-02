## `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:c8d2ab89cf6ece434d94a9f08ba15f17fa0a1d651e91894647b6ac779e9cf5b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5986f21e7bb5ebddb47f880f97d3e37a856a8e4304ea1fd20af45b6c53c2ff7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280799990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8dd59977cbc0cea6d5a608af95507252b4a5bf13f5141c36c9be037af8f4a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4403e3ea7f2a6fc4cd61e5c6690d620b3d5f7f91066d87917f5e4061947cc2`  
		Last Modified: Wed, 02 Jul 2025 10:24:18 GMT  
		Size: 157.6 MB (157634458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ab96a79fb053918281151db20eeda2b080efc2634e820d72d37e4c8d522586`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 69.4 MB (69409670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e3c9f0f5b3d97d5d288aaefb1747fffa0562e224d7b199c7e458533f57ab9d`  
		Last Modified: Wed, 02 Jul 2025 04:17:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1147379855d7b4340895a7b0423d9ae0b1019f45a4fd3117cb1f88cc9677e0d7`  
		Last Modified: Wed, 02 Jul 2025 04:17:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:23d6a7e04752e759c71a07ee228679bebff04d6043191fbcf10cc30513172b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af4890cc02324ed95dbcbef187be450ecb2902f0523b3cd3de3f10b0754c6a3`

```dockerfile
```

-	Layers:
	-	`sha256:c65bc9e52fac25879a04624b3dd44df94d8a435037e42bcdf4994982c3c426e9`  
		Last Modified: Wed, 02 Jul 2025 06:39:22 GMT  
		Size: 7.4 MB (7399416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20077ea8411f482ddd08d888ace8338cac5d45e939bf8afb0803576b1dd4870e`  
		Last Modified: Wed, 02 Jul 2025 06:39:23 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2d126d661db9a79eb809bfbbd575be5c42630c1e443070e0c4975ecaab4d1cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277719653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce16c3f4da0a6477f31e8e19f868a8376d46d08a0337f5af93191e4e7f7a8c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58e510cae3c2f52c0dcc3d8cd29b20a551d12ebcbeb7f0b7c1dd44e2de6a21e`  
		Last Modified: Wed, 02 Jul 2025 15:56:17 GMT  
		Size: 155.9 MB (155928828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34e3743e0efb9d2f505e89d6bed0b4ee7138d05f2d6774076d1cc364804f9fd`  
		Last Modified: Wed, 02 Jul 2025 12:50:38 GMT  
		Size: 69.5 MB (69537532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359f69baf8fca0ede4d98218ae62f905dc5183483d15d81cd74aeace452b32e1`  
		Last Modified: Wed, 02 Jul 2025 12:50:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2f3888aceb311c0447129fd1ef0898f9c25f0b382b025b02815b3ec4613933`  
		Last Modified: Wed, 02 Jul 2025 12:50:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d3e580ad6f7ebcc306097b923e9507b018a86af96353db62fe983bcfeb9ce573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0b14cc6a70a6000b808943b14c569e8cd9d3452d0a89b4dd732fa0b66f6a9f`

```dockerfile
```

-	Layers:
	-	`sha256:67f6199dc3f9d211faa18fd38154768a32336295e1ede1732ffee4bca990bc1e`  
		Last Modified: Wed, 02 Jul 2025 15:39:47 GMT  
		Size: 7.4 MB (7404539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c0131b867befb17440b359ac004a66ca98a95110cf17f4a2abd48cc752eb55`  
		Last Modified: Wed, 02 Jul 2025 15:39:47 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
