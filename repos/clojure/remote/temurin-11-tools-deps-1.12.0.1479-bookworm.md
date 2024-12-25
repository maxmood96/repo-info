## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:3c6c8715cf90cf06aaf1526e4deb77c8c41663081fc465ab1a636d79efee597b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:56f0308537a39cf5ea993ab34542a3899011b8b2aeaaee0d49b69b57631a5dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274843204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031d16c4b4d0a654f8b15e468d5ee51cee59af8bdc14f210d25809f7107ccdf4`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8d44ca6cc752b99923758be2367191ae97f0a90f471ef881774f6e435c53d`  
		Last Modified: Tue, 24 Dec 2024 22:37:43 GMT  
		Size: 145.6 MB (145601501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e507d8256b31f4ea7e2915508dd4479e7d98154c22d4f659274e793dece4711`  
		Last Modified: Tue, 24 Dec 2024 22:37:42 GMT  
		Size: 80.7 MB (80743995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733fb5d82aec6f8e91f4a433f4798b77625cc509ca59c3ba275086829da4aef`  
		Last Modified: Tue, 24 Dec 2024 22:37:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6aaaaded0d70f8a85df160f98bb7d0e8c0184b748959de1a6ab2ca1b93120950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a95482948b6888c29eec1d28a9667012fdb617f7c8da08635fdb75a1cce5122`

```dockerfile
```

-	Layers:
	-	`sha256:1eb51a0d99cf0e8b8531db53eb490191858daf7fd9af311d551b0c7e6aab5e7e`  
		Last Modified: Tue, 24 Dec 2024 22:37:42 GMT  
		Size: 7.2 MB (7191157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6df5d54444d960cf75160e9bf55631491b345d215ac085bf2e8cdf4576cb55`  
		Last Modified: Tue, 24 Dec 2024 22:37:41 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0b3630cc4a572f71cae9241971c15e22fb8a182328ab8163e8b1a3eb954a436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271319707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e59082961a08926da70067a7b24ee3e67157005cf92e431efbfb25bef870a9e`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b316b6da7602d7d947fb3a1a3a4cb0c5f81ac14644e8b0690e4182e479910866`  
		Last Modified: Wed, 25 Dec 2024 07:18:00 GMT  
		Size: 142.4 MB (142389012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cfbd72ec3055238a316a4039f7a7c55517c24187cc9953a9ab35db2a6123be`  
		Last Modified: Wed, 25 Dec 2024 07:21:37 GMT  
		Size: 80.6 MB (80604569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8787880f71f182a48a315dc945cac2378a06f205929945c253dd36b4644845`  
		Last Modified: Wed, 25 Dec 2024 07:21:34 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:104102ae1f6b424ab498deca64b25623fec158136393903559e395dd2cc251f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404c1b142624f2a34e908ccc64e8748ee8c5f5bfb91dc72943f4e05745d51ab5`

```dockerfile
```

-	Layers:
	-	`sha256:380ecf143950ad0321c1c37230bed713c7c9a836511d83e258fb2670c94bc121`  
		Last Modified: Wed, 25 Dec 2024 07:21:35 GMT  
		Size: 7.2 MB (7197538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4519c51389ed82321096762d11dca75957e438e3fd5044b38122c41b39a4214e`  
		Last Modified: Wed, 25 Dec 2024 07:21:34 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
