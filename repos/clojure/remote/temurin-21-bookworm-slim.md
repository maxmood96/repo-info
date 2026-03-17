## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:76d0c14b64f010be662e9cbb57b2580390aca43b6b886b0f1d3ec423f2897ffe
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:30c3648fc65e4df6a2096409881aaefda523b69d123095c873951c904c00cf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265590628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dc10c70de82838d22b42298c941c37fc5af5d80dc92af97c71ba1b1527452b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:34:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:34:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:34:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:34:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:34:34 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:40:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:40:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:40:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:40:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:40:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08aa22040562fcd55bbeb76a004a8c37c790885d218b8fc4c0ba2c08d72b2f3`  
		Last Modified: Tue, 17 Mar 2026 18:36:05 GMT  
		Size: 158.0 MB (157977514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df25cabb57ad1f950a08163ed25169c098ae555f97a67ae129c798995c4de8b`  
		Last Modified: Tue, 17 Mar 2026 18:40:56 GMT  
		Size: 75.5 MB (75533702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca536a2d7f4e827ccc9ba9609ca6b47e0afae8d67c1e5fd6930dd3dc6a6a918`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a954452be50da89565671c5e7fbe8b6ccadf6901a54b9b1922c9597c730840`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc89f23880ecb262aaa0eabf1f1ed26cfbc19fa40c676a6dd734a28c0291488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8459d2952507e288f589e95057d3ada724c3d6c9913f04d01d30a330e400f117`

```dockerfile
```

-	Layers:
	-	`sha256:952f133ae9a16f84e6d057850aaa166a84252a87ac60807caab1155410735f18`  
		Last Modified: Tue, 17 Mar 2026 18:40:52 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e89e643f591d4b7e54fb8a52bf5bec231b8621797976bc3dbcf9e51c96f058`  
		Last Modified: Tue, 17 Mar 2026 18:40:50 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:936d5243f04b3d1520a4f3480e8c03a2d9f00b7f7430842198a444531d73f256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242511662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb6ef3827845e3de77358ff45423b9bd792420b4cd83e2df1d6e9f1acc827c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:40:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:40:52 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:41:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:41:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:41:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:41:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:41:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868408284e96048311e29025e442c6905ac837ed90d9bb41b0e1ad914a79d686`  
		Last Modified: Tue, 17 Mar 2026 11:41:58 GMT  
		Size: 147.1 MB (147105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cdc5fe988a04ff796fb94ec08dd34ccea97f0f5c05ed16a610db5dcdab9d3e`  
		Last Modified: Tue, 17 Mar 2026 11:41:57 GMT  
		Size: 68.5 MB (68513894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2e2e82f2c8ca1be359ff9e8377c7865dec92335da7d33c3fb3863ad3b7f1f8`  
		Last Modified: Tue, 17 Mar 2026 11:41:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b0d0561e4bc19757fc2a28c89a74e5b992f62cc0a6324f2bb16e031b6dcea`  
		Last Modified: Tue, 17 Mar 2026 11:41:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7e764978338d6f1933559fc6bccf63c87c4eb67451bdcb56e081300c7d49b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68094e4ac67d10cb977e4c5fda7fabc9deb9b83909c38fa3123bfdc7298baede`

```dockerfile
```

-	Layers:
	-	`sha256:6b188f6ff7dd42b4912c293fccf56f36fb401d1addcd9f63dbf765fbf3527943`  
		Last Modified: Tue, 17 Mar 2026 11:41:55 GMT  
		Size: 5.1 MB (5109340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee810ed76d1ad85d1fa67d6c02a2e2c49414f73f639cb53b5b5eac5b3a819152`  
		Last Modified: Tue, 17 Mar 2026 11:41:55 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
