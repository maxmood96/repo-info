## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:3b2efc110bdf6f32c4fa35cffeb23a707b7314d6d165956148de8cbee3e57ce2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:904957793c962da992efa20b9c82028f78d39817011a15946b0419f868e81ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275069766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2244ab5e65a177d815cf5776b0207f264529a9e72433200e23e7a490e4ea0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fe8f811fe2c8e2b3cc67365a66d537a49fde4eba7c511fd3db0ccd655c142a`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 145.6 MB (145598934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ee2c44c2a6de65b311513924869f7d199a36408eccb0ee888eecd380f77f13`  
		Last Modified: Tue, 25 Feb 2025 02:16:00 GMT  
		Size: 81.0 MB (80994085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623ee11783fc8e11ba68c41fa1a9fb6f5a44ce0fdf8ed7174b1c6a9ec88fc81a`  
		Last Modified: Tue, 25 Feb 2025 02:15:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:af011e435634e5365143dd96f7f3cea570587220d2843691bbc42e9a5510bb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c8c20c677f1a6e7c8105f23ecf6e3040101032b23edea5cc02d40c5ccb2825`

```dockerfile
```

-	Layers:
	-	`sha256:a079a89d3ebc0f5a01a5a6ff20299dff539c2b5bbb17852e00b1532439ffaa58`  
		Last Modified: Tue, 25 Feb 2025 02:15:59 GMT  
		Size: 7.2 MB (7191237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d1a90f21cc517f897feec74547477a13cc7df4912a8f782c14126141213685`  
		Last Modified: Tue, 25 Feb 2025 02:15:59 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:910557bf24892e73ec72f0c262c7f46d2cad72eb799008289c136ae2c528af9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271538474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5143ff1d4c4d2c3b0e6d8d4a6f177588f71897949a766fa909c25e14bb61c094`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184623485b35c657e726514c4d2f4e673de25412f765279b47a5f77855967b35`  
		Last Modified: Tue, 25 Feb 2025 10:56:07 GMT  
		Size: 142.4 MB (142385472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a20e4ee03af8b9afa5983cbedd68571a3aed2521b164595cf0bea01310c1d8`  
		Last Modified: Tue, 25 Feb 2025 10:59:35 GMT  
		Size: 80.8 MB (80844349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00682f4138506e3d09e1233da113c2f5ae2bc3d6bc4a47f4af2f216cae8036`  
		Last Modified: Tue, 25 Feb 2025 10:59:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e24211acad3ec757a1e93f6951059a58c1660f7dad09b071a88ed8691d8202a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae73f23c157c17f56948312de1f41a1f4678ee1bf934d7b72a11a6274c1f8e1`

```dockerfile
```

-	Layers:
	-	`sha256:68222858a8887ba1d727c7e3a91057fb633bd824f20529997c8e293cc02323cf`  
		Last Modified: Tue, 25 Feb 2025 10:59:33 GMT  
		Size: 7.2 MB (7197618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd89f58d06af4abc3074a3170ab9849fd564b230978f354dc85e712754b9f78`  
		Last Modified: Tue, 25 Feb 2025 10:59:32 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
