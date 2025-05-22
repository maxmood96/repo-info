## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e4b87c699d2f887da484a9e62db99933a46f92ef4b937e921e9301cb39dc349d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bd795039795dbf9e5e01ed3acae97dee84d07e6fa93c6134dcb407f00196a6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246885704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0dd777654a647e0598f80ab9466b6e1ebf568ba33a0b28eba51568d133ebf1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaa41575aedf5aca1a4fcb81d6c008c0c21a3d293a4591ee2f940da5a9ca64a`  
		Last Modified: Wed, 21 May 2025 23:33:33 GMT  
		Size: 157.6 MB (157634544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1702a592e0bac9d28b46377a93b15b40cd7a58b7fbb3e45f8e5199e60af8c6f6`  
		Last Modified: Wed, 21 May 2025 23:33:32 GMT  
		Size: 59.0 MB (58994179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1983cf53734e7c8897db1727db79a6ac02b9f046a2568a3746e4d09a19577a2f`  
		Last Modified: Wed, 21 May 2025 23:33:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309cab1750a1525618797508169ff95b252dc4397c7571f6ed4580169c8334dd`  
		Last Modified: Wed, 21 May 2025 23:33:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84308a3d160e09f8bdae597e090e1daf131759d3c5c42347510e428d1dbb94f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccd3931e1922f776bd2a100946c76b1ba6cd53a42fa08661d98ffabd46353b6`

```dockerfile
```

-	Layers:
	-	`sha256:95c1a81737e3c493ca96bf88ca37ae778429d2acde2a76ba115d7a7f938491c5`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 5.2 MB (5170788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c0d083d99939bc509a853571e7cb435842c5756848329700e8e6864a06941e`  
		Last Modified: Wed, 21 May 2025 23:33:30 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91d4429e152a4ef12cdda1f1c22c8aa83ef90eec350facd6ba0b74134ad97f`  
		Last Modified: Wed, 30 Apr 2025 01:47:24 GMT  
		Size: 155.9 MB (155928805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

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
