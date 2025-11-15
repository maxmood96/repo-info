## `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:a706d268f0a31fbacf58cd8eec4ead0f714ea031f284f7509b3ac6e571393836
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:143dd4efd9b872c5b0eb2bde8aec7c5987fd0934a35e0711136c9b2720830211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268284964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f53cc7b46c7063d150409f57fa4b41823f056ff5c0291e2e4f0bc8e06908fa3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:51:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:21 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f61acf7857a01360e0dcac8799f28a5c67b42fdce3cddd1f6b8f5cc8d566920`  
		Last Modified: Sat, 15 Nov 2025 10:00:13 GMT  
		Size: 145.0 MB (144966578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f2330a4b98cae102a9538814baf713554992ed3ec382465fb43d9397e18a52`  
		Last Modified: Fri, 14 Nov 2025 00:52:14 GMT  
		Size: 69.6 MB (69561045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b51f6c64e73191ec347cd96eee9822b0767dff801696d366ef1cf33efbe2c0`  
		Last Modified: Fri, 14 Nov 2025 00:52:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ff0f18bd1b7fb7fb7434f09b17a1d8b836a8d6de4e3b33b8b89a4d43cf9b6c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3139df34e57f9b09a48c3807358fe538766921b93155a1e024962097c6cdaf68`

```dockerfile
```

-	Layers:
	-	`sha256:477367b2ad74d83378f9516fe872879ab7ebff5b9caccbbf791bdef85ec7f3bc`  
		Last Modified: Fri, 14 Nov 2025 01:35:42 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea565eb905c17fafdf39957e00513d883a8f95df1fa78f4d03b6bb9824c4b74`  
		Last Modified: Fri, 14 Nov 2025 01:35:42 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:01b13b6873c7604346933663a6230752a4f4e265b966401209943d61dc41218d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263678439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed3138d3720ff4cd0d2233e65c737110b0c02b110ca039a909cc4dfb5f222f2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:53:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:28 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0cff78ce7da2c5e5c6538b9c8adbf5b6be1bf40da29d545f9ca4440037aa98`  
		Last Modified: Fri, 14 Nov 2025 00:54:06 GMT  
		Size: 141.7 MB (141731502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d852780fad37e29b1cc30efa3b6bfcede882cb26ed96877b02b90d9f37e920`  
		Last Modified: Fri, 14 Nov 2025 00:54:17 GMT  
		Size: 69.7 MB (69688323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba561bd3261ddcc853fc33f34508dee04382853e9dfdf032421528245cbf1c`  
		Last Modified: Fri, 14 Nov 2025 00:54:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:33111d6dd07ea9a71e07c8a19a52207701a592804b5a61f9f522a255716839e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6bfbe18c756820f13f05f914351d8f135276d81c100c2dc6d64de0e6da5c`

```dockerfile
```

-	Layers:
	-	`sha256:1139530613827e4fc70b5bd5720afb9ee84334e7785a74b9c211a4cfc74a2664`  
		Last Modified: Fri, 14 Nov 2025 01:35:49 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a11a436dc75dacfeec837a61e388f76895a659b179e7005bb57ff932d209d0`  
		Last Modified: Fri, 14 Nov 2025 01:35:50 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
