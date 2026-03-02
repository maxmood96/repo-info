## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:3ec7a60b69f886fe98166c39ef090e464949073ff724e1a4024733927003b850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5a115950dcad06ab1a2c81ee9cc5ab301f2efabb9b6b8de29e072a5a5d88cd6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281199519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8aaf137ca3f17dbbf2740fe8484f3359da8c65081a00de87aee9e0eecd0b12d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:47:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:34 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:34 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:48 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80459a9d1caf7054d123855b2fce429c3f091ab3007af1cfa10c2a472e2110e3`  
		Last Modified: Mon, 02 Mar 2026 19:48:12 GMT  
		Size: 157.9 MB (157857123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90e4e971008af90ae2089f774ccbacbf4c9276a5cb0027d3ae0a2a5e898efd5`  
		Last Modified: Mon, 02 Mar 2026 19:48:11 GMT  
		Size: 69.6 MB (69584922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682058a070c5c881583734ea3983504e0897efe9aa6033efb6922e2b2b98c47`  
		Last Modified: Mon, 02 Mar 2026 19:48:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbb4f0a11698a4e01e35f2b9cb774c0828df7aa69dccb6823d1e3c57dfb927d`  
		Last Modified: Mon, 02 Mar 2026 19:48:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:20a571aace9f811175777d3dbf744913bb1e63e298d9295909551a00edaa772f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399f1dee568a7073698c1ee55bcab69c0c1781f36d1bc4611c2150ea688aaa70`

```dockerfile
```

-	Layers:
	-	`sha256:9ee329fb645f20841ac8e56e111950c262b76689c3259709e67c6ad4a131321f`  
		Last Modified: Mon, 02 Mar 2026 19:48:08 GMT  
		Size: 7.4 MB (7411129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ad07e6973c6b14e50243efc424faf4d02ff5035f0c5b65951b052afacacedd`  
		Last Modified: Mon, 02 Mar 2026 19:48:08 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c30b30ceb170e93fc8f105a5f3e862056d70b0ac67572c9eb8a0dbeeee294206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278118049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f2035a6e0108c1c742508c96b25c09a57802df9a34723820ab0d06a82c7b10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:27 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:27 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:40 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16609b8ef7e33ae52ae2495151fb109caad6bd5559fc33e69ed482841f6ed6`  
		Last Modified: Mon, 02 Mar 2026 19:48:04 GMT  
		Size: 156.1 MB (156133063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071102220c244546d89647cfbda35fbe67cf96bc765545fd3cb2bdb79cdeaef6`  
		Last Modified: Mon, 02 Mar 2026 19:48:02 GMT  
		Size: 69.7 MB (69725551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce3ca9952e3538f3c09ee5ee21f804e0c03d9fdf269120f3797bf16f2d2760e`  
		Last Modified: Mon, 02 Mar 2026 19:48:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7bf20201a89aa6287403b5cf1892af1d8d3342142b6a0794074f339201543`  
		Last Modified: Mon, 02 Mar 2026 19:48:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7acbc969f2368a95e6e3c89976222d57fdf90c515ec36e7a866952715b25c1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2405d9e69c2bd0dcfd6d617508f2fff2c845e7668950cf20dade5165f8cec2ac`

```dockerfile
```

-	Layers:
	-	`sha256:76a0e429d62bbbf55844bb2b6934a1bbb46fbeb6c5b73f28074693b36fb3ac83`  
		Last Modified: Mon, 02 Mar 2026 19:48:00 GMT  
		Size: 7.4 MB (7416228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b483a43a9ee08a2c3c52722525d04d451175b6899537bb01491bb57d9796b4`  
		Last Modified: Mon, 02 Mar 2026 19:47:59 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
