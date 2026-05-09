## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:8415b75a224c2e672ae055a092853748789ec552e64bfad59ffd0266fc0ef64a
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d3f9fcaf34b97bccd271ed185e797c36cf0d09284a270af0c5aa480053b8521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280759816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabf086c4a14dff25429b22b0da9513c8730fe6de306c2c5e769bcff2c1ad7c2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:16:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:16:24 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:16:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:16:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868e7572717ffcfa178eeb327c4d640d8905a85b451aa265d87c63c2b943738a`  
		Last Modified: Fri, 08 May 2026 20:17:04 GMT  
		Size: 145.9 MB (145886207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44d84e4d47040fedcf5fbe484eee4db1816e594da1bc7d809669b040cbef831`  
		Last Modified: Fri, 08 May 2026 20:17:03 GMT  
		Size: 85.6 MB (85570646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecd95c8f273f056afa982f6c95f410fd81a875f40365e7f150b81b22aa369c6`  
		Last Modified: Fri, 08 May 2026 20:16:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0a7f392af5e6ff8f8cc82d48255a4158794b3ab89dbef816d5293bb86a2b237a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e1cd4ff70870d8e9981a90dc0fc605c55a5ba8784ca482ba389f57ec225458`

```dockerfile
```

-	Layers:
	-	`sha256:30cc7c8dca197d41639abb17a4ee18e183abef35ca787ce0464b7a1fb6f2bf59`  
		Last Modified: Fri, 08 May 2026 20:16:59 GMT  
		Size: 7.5 MB (7490864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76aefaeb18521c691bb0eae235777b69810acded1cfd51c2364237d74b433949`  
		Last Modified: Fri, 08 May 2026 20:16:58 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59492d4adff23c5b3be671470239bce8fd352cbaf7b7b80c53e06b9b12a8ec15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277635951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99b24f073b50d7c5d2d0672864a55cdfa2c029dd1febe57c9e84c1744ca2de7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:39 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e631e0551ff0905c37aa64c13c3eecb59e9bccf9bdcaae8bc0baf1498649c23`  
		Last Modified: Fri, 08 May 2026 20:21:23 GMT  
		Size: 142.6 MB (142582247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426c53b3c2aa77fff7b8f02efb3db06386036328ff77da17c88f86396d73adf7`  
		Last Modified: Fri, 08 May 2026 20:21:22 GMT  
		Size: 85.4 MB (85383615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c13cbdc9aabb4f40a2dbf429e62ab8b431c6f71a9ec8b69723abf90bee37e1e`  
		Last Modified: Fri, 08 May 2026 20:21:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:29f2e71acf7e5c7bafb16d02f20be6b52465f921bf8bdbba578f3d6948e7eb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385a55655cd38690e1557dc3459409b0fbd7ed5fdcf304dbbaf155354abd18fe`

```dockerfile
```

-	Layers:
	-	`sha256:3aa9636f37a1b6d8ca5760d87bbe91d588327f328c44a9e6ee79f4768da880b5`  
		Last Modified: Fri, 08 May 2026 20:21:19 GMT  
		Size: 7.5 MB (7498512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d8c7070540b1f85949a2c99e3e67c2b830b8d43e2ef2525cf0f3382382b865`  
		Last Modified: Fri, 08 May 2026 20:21:18 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:cc055f0d4b3f9ad69e579ed1b8492acc09464a3ba28408d3566ab254ba8396cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277220549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddcccd73f31f0deea58cf2023e254c041ad19de178cf4c2990b1e3d465fe338`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:26:20 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:29:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:29:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:29:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6819a6f95dd2e4192ab6b7dae90a40976321dcde2fda4665eb71bbac73d5122`  
		Last Modified: Sat, 09 May 2026 02:27:27 GMT  
		Size: 133.1 MB (133110167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2de7b73d106fcd3c69fb749b493b40ab7e2a4f54e88a69824ea1760e4f512c2`  
		Last Modified: Sat, 09 May 2026 02:30:08 GMT  
		Size: 91.0 MB (90986570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18f24588bfef6a71d298ba030dfcaa8d7a5f72adee9250caa5324a0c05b9c16`  
		Last Modified: Sat, 09 May 2026 02:30:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b9fa1fd1692f2b554c82a3db45492b3f3681ed40eba63aea2b219e43112f0635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992138e69bce655394ec1b0b1d00cdcfd471cfdd1c010da881c585dcfa8cb98d`

```dockerfile
```

-	Layers:
	-	`sha256:15161d41c7efdbfcf8608fb4e2e64852fa30dcac2d7c41c3a9fbc84c3faab633`  
		Last Modified: Sat, 09 May 2026 02:30:06 GMT  
		Size: 7.5 MB (7494670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0904c9e28c8e3b76a4b96bcd84e5d3891ec606660d6546479cc664cb8f420fdc`  
		Last Modified: Sat, 09 May 2026 02:30:05 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:603d9b08bd1484987aeb0da070b32d70f66aaf9d53eae5ad046730a56cc6e041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262570006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f165750c4ed2a1db84986c30594c2a6efd71aa786e8ff6b1c5dc04fdd16ebbbe`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:13:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:13:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:13:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:13:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:13:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:14:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:14:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:14:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3141bdc6a188297dcde1fc53d547484d702825156fc236e4ab9572430cd65294`  
		Last Modified: Fri, 08 May 2026 22:14:07 GMT  
		Size: 126.7 MB (126651743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc614bc86ca922f06a16629ac07dfa1c6b71a0ebcf6a27b906c4416b81c66473`  
		Last Modified: Fri, 08 May 2026 22:15:12 GMT  
		Size: 86.5 MB (86545316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ab34345b0fcabc7815ae26c8450a40dfcf9b147c2ad51323bab76b5e5dd5c3`  
		Last Modified: Fri, 08 May 2026 22:15:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:82058a71af7656c3934fcd7854f1e83ba25e8de997ec342b914e8e8697fe0d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bae20fe91cb3dacfe6321bf54110da32012d19c9a734bbfa8a7c1401c775a43`

```dockerfile
```

-	Layers:
	-	`sha256:26a291b12b88115a4453094558b3e512fe8e63b8e0462222e35cea281580f314`  
		Last Modified: Fri, 08 May 2026 22:15:11 GMT  
		Size: 7.5 MB (7486790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5e8338396e093e86a45c0ddea2f70d97548ac1c86577749d4c0b501ce78b09`  
		Last Modified: Fri, 08 May 2026 22:15:11 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
