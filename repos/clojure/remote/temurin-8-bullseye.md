## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:0d3b737f3361b0c66ddba34f3011efcfc978e232d9de93714b521b768b5cd39b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:887f8e5bc0a566c620eb1b8c7ca6d8995f064a54b6a3bfd9bbd5ec297f09185a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226552261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6740a2e9ee31062916e3ce9f258d29f8541b7d55e51e62f6e4730c9179ae0c72`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ab2c0dd769b2bf387d56de9cca7dc0752851f6320d1fc6f761f44d1b4dfc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:20 GMT  
		Size: 103.6 MB (103633885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e115ea76505e8a7174cf381537cce07b2432641e7b0e1be9aa44c096eb255f`  
		Last Modified: Tue, 14 Jan 2025 02:43:20 GMT  
		Size: 69.2 MB (69178568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad84f22b321e68dd16ca54a7e608f8fce722ef1229b3b18cc4779ff0f4ec4a3e`  
		Last Modified: Tue, 14 Jan 2025 02:43:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6ae237640aad812f434a56418ea07d86452fae1948c188fa52b9e9dc1caa239c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947653c877f1e5e3aa6cab4cf4996cb27b1719045a40ac1b48490e1bc96f94c9`

```dockerfile
```

-	Layers:
	-	`sha256:98ab25bfe71456176b1c65c0d34cf514f1e081af162cced0144b1d8e015dca02`  
		Last Modified: Tue, 14 Jan 2025 02:43:19 GMT  
		Size: 7.3 MB (7326775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8a2351b0e6681ef70eb3441254ca2863e51f7268447eab30c7dfe77855f3ed`  
		Last Modified: Tue, 14 Jan 2025 02:43:19 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78ae09bb42e501d081eeada137ffe149737bd8056fbe0d06d4c47e06b4762009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224298958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f0c41ea1c2895356410f1edd3a069e8ace33c1e34ae3dfeb36bee419e67d55`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f468498da49c43dd921b0f405aeeb87eb714221124b311e09a623dcaca2d6c`  
		Last Modified: Tue, 14 Jan 2025 22:03:36 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6817bdb8894774d6508b1a4657450732973b7097552ebc5b7bc0c48ac684ad4`  
		Last Modified: Tue, 14 Jan 2025 12:18:35 GMT  
		Size: 69.3 MB (69304538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc92b7f7ccca2923c202cae942f8ffe1919b64bba9e5da46f31b855dede5ede`  
		Last Modified: Tue, 14 Jan 2025 12:18:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5ad5ec67d8ada9b79f90ce14f0df1cae42ec622f22a6e5b82680ccfe01cd4b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af294e72efd6aa4258ad0868f8ffd322115e5abf914eaf05fb760d8fd3521b66`

```dockerfile
```

-	Layers:
	-	`sha256:dc5adca47148baa2651cd984e54eb8ac88f43cde75832220dcdc9e4dd1237518`  
		Last Modified: Tue, 14 Jan 2025 12:18:33 GMT  
		Size: 7.3 MB (7332572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3467456e73526610de8e14b69fb09278b81a423048c6fa522acf9e9f607d4dec`  
		Last Modified: Tue, 14 Jan 2025 12:18:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
