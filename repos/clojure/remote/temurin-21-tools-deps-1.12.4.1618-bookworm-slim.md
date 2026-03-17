## `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:9c2bf6b6c33955e81a5ed3d51375c6a151034fb547431434fc069dc5085230b9
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c4c4e239ebd5af0c99a10faf1260970994031ecdbd73fdd5ea8889b05445b1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255796111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a668ae1570e36d8741c9a10394c773b3cda5e182b10bcdb7b8b5d821f13ead`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:59:40 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:59:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:59:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12daf5522a7c1708934201f8ce618e76c388cfe91ad7e92f983e1d1dc626651`  
		Last Modified: Tue, 17 Mar 2026 03:00:16 GMT  
		Size: 157.9 MB (157857083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dbbfe270784f3486f778a80ec5041197bf4a2978133a4a56640401bec1355f`  
		Last Modified: Tue, 17 Mar 2026 03:00:15 GMT  
		Size: 69.7 MB (69701764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38994ca4364a0f9d29a371675855636a6d00c806c25ac1a6d2f571f007dc7833`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be6395a600d272a8ff53f0ae15e15004cc85e6f8df72ad6e9578dea14557010`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf001aba20bdc9170d7acc665c3f319d5e288bf25fac12871e70f1e474b9133d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72875d5f01b9a666c5f5c8919cfb0d90c78b118a0ca72c5252e7a733c7e039f`

```dockerfile
```

-	Layers:
	-	`sha256:72b6f450795378108c0863e3677aeda34fadebc0c1baa4f9991d0dfb5b015064`  
		Last Modified: Tue, 17 Mar 2026 03:00:10 GMT  
		Size: 5.1 MB (5118019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620091bde16cc0026f3be7ed8843055fed13bcd2fd2a8bd677f5a1112f3be178`  
		Last Modified: Tue, 17 Mar 2026 03:00:11 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61c85a129a5c4d3faadeba844e44eb5b1976ebe81eef36275f93c86f09ab2ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253939133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5b1b0494ca88662bfb7a42a6658b657c53d52cd0159b4336aa2acf9f4692cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:04:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:04:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:04:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:04:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:04:25 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:04:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:04:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3985ed1b4438405a3db2c57275a13d9bb647050347dd2379494e42f0a332ac88`  
		Last Modified: Tue, 17 Mar 2026 03:05:06 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be668c48d9b53dfac59a4e01b6f524ad38a4000490ef0a8ee0d35d8362c27568`  
		Last Modified: Tue, 17 Mar 2026 03:05:05 GMT  
		Size: 69.7 MB (69688960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2c4bfda86a7731646fe30971e02c0715669e3209bcd210d30af38a6523008f`  
		Last Modified: Tue, 17 Mar 2026 03:05:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffa73e53511aebabd18997f7a51ee74367a697eb8c3f5e136ac51eb509c856e`  
		Last Modified: Tue, 17 Mar 2026 03:05:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7cd7b6eb6ae3969c4ce77a0a2905b98dc80745bdb542be55952dc90b6e4b344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b03bcdeac28390df6f2bb1c69de8ae25bbefc6102e28b509ea68a3fcfeccda`

```dockerfile
```

-	Layers:
	-	`sha256:a0cd2bee25291cf59ca2bdd4c7f6e511e96536a68a83c27b674365bef6d4a0c3`  
		Last Modified: Tue, 17 Mar 2026 03:05:02 GMT  
		Size: 5.1 MB (5123780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b9954682f0045808a7fc7ac44987e05f3fd8e0f4e2ed9f33304a79882fb3eec`  
		Last Modified: Tue, 17 Mar 2026 03:05:02 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a574422f7b504518d0e47a657281044c27bd3a5a1add93bac02447bb3baea568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265590493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26c07469aab196314bc9e665cde18db78f33675e4bf32f21cdb187ec5ecf993`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:57:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:57:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:57:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:57:21 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:58:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:58:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:58:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:58:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:58:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa55a66ef4e8dff32d0371fd3807d5854e51d4a75ac606239492131837d03381`  
		Last Modified: Mon, 09 Mar 2026 20:59:47 GMT  
		Size: 158.0 MB (157977536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8163e3c869ffa6130478bd7620c8046ff5c544c1da0e98e1581c3682276b80f`  
		Last Modified: Mon, 09 Mar 2026 20:59:45 GMT  
		Size: 75.5 MB (75533579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1208cac526fba2f3e03a17546ca2f13f04c292adf265081b0667cf7419e47ea9`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b99af08417eb307a4c17b9b6fbeef8f1d6a475c28d5bdd5a044f5eccc9beaa`  
		Last Modified: Mon, 09 Mar 2026 20:59:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6b9e6b11c446857deb10e8f1c2f818eb7ed6dafe5f02a5a43d6db3d971719cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588682d8b88e17c830bd78da1e70e696e1181f679ae6b76d5d6e97e147e9508c`

```dockerfile
```

-	Layers:
	-	`sha256:ac23b461c7f805e7ef9ac314ad2fd5d868c76e6f841a0979de535cda3f8e2c99`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56810832478ddb66b72f648252a0e4d593f51229629890ef54eaded600a589a8`  
		Last Modified: Mon, 09 Mar 2026 20:59:41 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:012d2b323a7ca3c0b66d6653f83be842fd73540fdf8166afb38e84c6e2289227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242511705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1a810aef1d7ed0bc3920e48d824c566778961f6bee34ac5fa0fd4b05eecef4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:35:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:43 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:57 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b466334a4053e88be58806c3c50040ef435b541b329f108951325c103a7d6289`  
		Last Modified: Mon, 09 Mar 2026 20:36:35 GMT  
		Size: 147.1 MB (147105306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94931f047d359e1798322a53a7bcd4d778a8ce8b78d3c5eb062ea830a638fb6`  
		Last Modified: Mon, 09 Mar 2026 20:36:33 GMT  
		Size: 68.5 MB (68513831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6688adc180e311222124593a154c02ad802e7843f52068d1b9ecbd15945720c`  
		Last Modified: Mon, 09 Mar 2026 20:36:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9572d462051c612074186973ca0b0348bbe832f1a18062d308edd1be2e22d7`  
		Last Modified: Mon, 09 Mar 2026 20:36:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0688eb545e01252ff7dd987099b3a404b1edc068c39c79e02a4ae71ad302ad4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51aa1b297749661d6a191c1a2bddb0dc19fdd73717a7d8a1b85ab50bd9fe6445`

```dockerfile
```

-	Layers:
	-	`sha256:e832c0b1a85d539dac545279d2f25ea2f31757d2c06ad2caec5db1d439fc5af0`  
		Last Modified: Mon, 09 Mar 2026 20:36:28 GMT  
		Size: 5.1 MB (5109340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59ff43dda218f933259adca2773c39e39292e5ec73fcf409cc377bf6aaec49e`  
		Last Modified: Mon, 09 Mar 2026 20:36:26 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
