## `clojure:temurin-8-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:dde6b55d41f5d8574d89d1f7cd1b732422e42561ab5a3e184ffec25508168591
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:85ec35a0a3cf66cfcc9f5924fbbae285cb36eff10e9b811b679679d9f5a141c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189560142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fd34310695b8246723bbd6a158e3c65ae024e02ac3552a1186a92e2110156d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:50:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:50:14 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:50:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:50:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:50:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44776c398f950e86b0cc93bd364cd6993b9de780bea30f374194013bf31e5612`  
		Last Modified: Fri, 14 Nov 2025 00:51:02 GMT  
		Size: 54.7 MB (54733370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faafab52e97e6dbdf4aced376d5f6bb7f2caa08de486323760708c00f165737`  
		Last Modified: Fri, 14 Nov 2025 00:51:10 GMT  
		Size: 85.5 MB (85540498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1b3a363d419249c27e7b138b7653c055d58303876bbfa1ec9007b61792791e`  
		Last Modified: Fri, 14 Nov 2025 00:50:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c49e1d93c1e4b08b17fac1e31253e636f00ebf5b34574b180e28d3f687ea997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffc93a8e1ddab6c19baef4180cea7cc6b6b3ba535d8df8343a527aa973d5bc5`

```dockerfile
```

-	Layers:
	-	`sha256:1ac785f8d4dcef5dd7e11a8c8a9f5efcf84cd2e21abfb0f31053462324ed9d26`  
		Last Modified: Fri, 14 Nov 2025 01:51:38 GMT  
		Size: 7.6 MB (7588509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea0c158e6508a7e7bc48fb0f88d54d3e44e71f1b670ae7ea440b5b820d031b9`  
		Last Modified: Fri, 14 Nov 2025 01:51:38 GMT  
		Size: 14.2 KB (14168 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31e031fe97b1ee9b5f6df899b8050c92b0ff6405dffd16a3efe167b5f068da72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188829616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0198b40cf6eef573fe373ead98bfc1d3106ed897f7dfe4e8c52691188f478190`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:51:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:17 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:52:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:52:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85b9b1a0b8938b79f275e12b34be8f0558c34dd0bf62e130debbd7f81fba9a`  
		Last Modified: Fri, 14 Nov 2025 00:52:03 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01acfe3bc4c5fcafa6efca600d76dc9999b365b626ddb878acaba0d0125e5989`  
		Last Modified: Fri, 14 Nov 2025 00:52:50 GMT  
		Size: 85.4 MB (85363544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b9d00f555969f97ae085339559f714bdfd5eb6e1c8be820868de99e46a7346`  
		Last Modified: Fri, 14 Nov 2025 00:52:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:09416e08e5ad34d1316708f2890353ac2660189f592e875b41310e044154f724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7609724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20df93af7e69e378327608582c5f439a0369c588c00da3537a9b3324e819349c`

```dockerfile
```

-	Layers:
	-	`sha256:14b979bae5442aa24c940d1f5cfaab9de1fef58530395dc70d3201a7277c2541`  
		Last Modified: Fri, 14 Nov 2025 01:51:45 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555510ba60f509bed31af29d4a2c6b54710dd72007100e0cf484429141faa9b8`  
		Last Modified: Fri, 14 Nov 2025 01:51:46 GMT  
		Size: 13.5 KB (13487 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:eac9e2a3c390b8e7b1c4fc03bc1e717e520bfb67ebd4a0c0bdf76b2918deb7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196235578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae530c95dd45593f021c606d77beb9e015606e00fb746b2f81f1f6e75297518`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 06:28:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:28:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:28:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:28:58 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 06:28:58 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:38:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 06:38:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 06:38:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb675e244bd092296b45305c4b3f2ca038199b80c0f01e0ecfc7844547ac53f`  
		Last Modified: Fri, 14 Nov 2025 06:30:27 GMT  
		Size: 52.2 MB (52175150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acae8cb8f639ab13e62b69d68bb70c55192bbe95c5055c3068064ae9557eaa28`  
		Last Modified: Fri, 14 Nov 2025 06:39:59 GMT  
		Size: 90.9 MB (90949654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f964277824de033429eaf96183c381350ce20598f6405d631a53aac30284b9`  
		Last Modified: Fri, 14 Nov 2025 06:39:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:37b095e3c74876164d20106c82aa2c760249b1d6b04a9b0c0ddd4d9856fbc5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f419c1f5e4d0e70f0380f2d378ff424d1144fa4f5deee42fab5d44bf7c68db2`

```dockerfile
```

-	Layers:
	-	`sha256:11b62b6ce1965cb2cc1f313fe894249bdb6a45187f2a00228454384be0634a09`  
		Last Modified: Fri, 14 Nov 2025 07:41:05 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019f035ba6fd9d3d38ad416c099a4b82ecfa557798c556f447c3978badb09652`  
		Last Modified: Fri, 14 Nov 2025 07:41:07 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
