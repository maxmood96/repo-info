## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:d4097f386ca2545b880cb816d74357c35d6f0c417c8bb1c77af4e0ec69aaa446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:92e53dc8b5bd497ae6337d98f051d036a8928ec5b871c3e5e2d63370d4431ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144144327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaeb82ead7d0164364f729a75b3544bc0edfa95469b08ed70c92728cbdc600c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:49:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:49:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:49:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:49:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:49:17 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:50:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:50:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:50:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b16603dbd2a7fd24ac5f08c126803495fbade9827adbde922f7fad045be272`  
		Last Modified: Fri, 14 Nov 2025 00:49:58 GMT  
		Size: 54.7 MB (54733322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45b4ef0fd9e9dfbf9d9f8f9c340e66193cb9472481156706da2044d01150b61`  
		Last Modified: Fri, 14 Nov 2025 00:50:32 GMT  
		Size: 59.2 MB (59151763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999126414a3a08606851454213a2b4e9c3a43cb097ff7c651401c9bd33b84849`  
		Last Modified: Fri, 14 Nov 2025 00:50:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6dccfa36bfb3ad39257a10e5547754e41ae299eb772a8676b9ae10ac0815e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5767becbc87d109a66ca04753d1ca4d9258d422c137339c3f0af39bdc7a549b`

```dockerfile
```

-	Layers:
	-	`sha256:34ff70dc16a6ed14083a42430e7defc5dc90fa730e54f2abe3433b054eeab77d`  
		Last Modified: Fri, 14 Nov 2025 01:49:32 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9345697c6607f96b195d47e6d557641883d2eb64d19093cdf3ba3e2889348ea9`  
		Last Modified: Fri, 14 Nov 2025 01:49:33 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8b3edaa05d5adeb6147bba2ab405c1e327a0c1dab8c66db7b9769aacb2f85e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141851798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e790d0d20c4c2dc7dcd02a5994071eb3594f73a941d7ffdbe4f3b13d7d00a0f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:51:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:52:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:52:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6b5ac12771bfb0c91ac6b9ac2ae31308f6e687b68770834f50b0067726c16`  
		Last Modified: Fri, 14 Nov 2025 00:52:36 GMT  
		Size: 53.8 MB (53815029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38abf0dbdb609f9e2058fdc5d148ff3d208bc1f8c92e2c43a391b2f7446dbf00`  
		Last Modified: Fri, 14 Nov 2025 00:52:38 GMT  
		Size: 59.3 MB (59287569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c05ab1cb27d324460602fcb919d3a7aef1af37eebf905403d73073aadee2efe`  
		Last Modified: Fri, 14 Nov 2025 00:52:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7bd3b71c20a1b7476f038d756731f1e8ecf6c86ccd27fc7cadf74dc1a8d402d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424e367bbf170e75b55c77e1bce5755cebe91cd14952dc08e3dccd763b20aae8`

```dockerfile
```

-	Layers:
	-	`sha256:575e5cf50ef2d1df2e1e7602d84d52f788c48b897bd852d193b28502591d8e24`  
		Last Modified: Fri, 14 Nov 2025 01:49:39 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4761b43246e6e294e74542c91de22a116f6ac71b23359d9021df7932ae642ee8`  
		Last Modified: Fri, 14 Nov 2025 01:49:40 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
