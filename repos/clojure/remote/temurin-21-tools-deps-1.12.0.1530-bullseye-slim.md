## `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:94235d469e800921a652d7c51906d4fe79e5fcd120545b1b9e6bcfbaebb90499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c858108a738d13d6fe006cda4a758c2d124f9be3eab450ab383080cb08c6a369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246882973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff00c32299d6bbf87c2f7a5d2408a973a7b89b1a0957384c800b844ede3705e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e51cfdbb01293c45f264bdbb2303ae458cbf914e8d8c66ca2331b6b8d93757`  
		Last Modified: Thu, 08 May 2025 18:56:12 GMT  
		Size: 157.6 MB (157634380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4002db06c1bba3eb4929dae729480d44aff593c3a9ecacb8ee60fbe005280c95`  
		Last Modified: Thu, 08 May 2025 18:56:08 GMT  
		Size: 59.0 MB (58992948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d1bb4c17122284949a334801482622892dc006bce7b96c4aa205050cfc6d6f`  
		Last Modified: Thu, 08 May 2025 18:56:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df71102ee2c44be3f1a04b9a70642583fcd2de1586552da5d23304a21b6887`  
		Last Modified: Thu, 08 May 2025 18:56:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb861c1f6c1d9d81f54a5a65a98557b11c593dc437bbf7ef083b574bd511dfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0646038d58754349aec178b0a280d31a005060c5292d4f7afb49aeb87d9dd2`

```dockerfile
```

-	Layers:
	-	`sha256:dc06fb71af1531bbaefe5ef3c829394d2f181d24a02e6b7e852d0eac9d155062`  
		Last Modified: Mon, 05 May 2025 17:07:48 GMT  
		Size: 5.1 MB (5122865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848b3427e8d1dd1bc68dc24ccea2d8f332b95cb53c6fd805324b38d0d2208d29`  
		Last Modified: Mon, 05 May 2025 17:07:47 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5fad444f18208e29bcf4c1fb959f418245615f0f82ded2157dc40f64ecf287a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243801917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d3043de1c52a680b22a23fce71e4d21482c619fe923ac85de97956ac8a4618`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91d4429e152a4ef12cdda1f1c22c8aa83ef90eec350facd6ba0b74134ad97f`  
		Last Modified: Thu, 08 May 2025 17:18:14 GMT  
		Size: 155.9 MB (155928805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd1d9c263a8a93ec043aa0f594fea8819404d18580ad86f9c2ae4069fa1f34`  
		Last Modified: Wed, 30 Apr 2025 01:47:21 GMT  
		Size: 59.1 MB (59127431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0271c0776ecd01ae2415bd72c0f214ada008f1c3c22c744ce07430fef0f58e`  
		Last Modified: Wed, 30 Apr 2025 01:47:19 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e1df589385fb0be2457031f8449ee88aee0557ed6d80135f7c97431398ca64`  
		Last Modified: Wed, 30 Apr 2025 01:47:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b33dc17329a4118a28db0d1bac279033dd0548b85ccbdc71a8e958b9c164fb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a570d4b5590aabd5fc152677fd6eb66309279ca765eb1502f9e9e4d8b1d43a`

```dockerfile
```

-	Layers:
	-	`sha256:d59ab2ceeab7cdeea2ef882fc631bfb5f58e2ded617451ade89df00fb8ff4d43`  
		Last Modified: Tue, 06 May 2025 00:45:02 GMT  
		Size: 5.1 MB (5128621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0bebd7272211e3229f7f61b26416e8b471def2dfdc784f2f03d627055e7f1f`  
		Last Modified: Tue, 06 May 2025 00:45:01 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
