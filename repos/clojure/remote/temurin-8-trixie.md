## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:f2b8aec7de841280d5f992f2521a0856155add53a5a7281421fee92752ec05c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

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

### `clojure:temurin-8-trixie` - unknown; unknown

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

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-8-trixie` - unknown; unknown

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

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:75de82795742efd48bd96dddfbac17aceb496102dc08ee17444e4356440bcfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196235400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fe746cbd2722f9dd71756d5569559c6db7fdee9dd711d25aed4564293853ee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:11:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:11:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:11:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:11:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:11:40 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:21:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15756aee0cd03dba616edf460afe9c03ef7dde5b1013400db300db86aaac11c3`  
		Last Modified: Sat, 08 Nov 2025 19:13:28 GMT  
		Size: 52.2 MB (52175136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2099dc2bef0d8cd485a5098c5e1c3d2adf26a5583d7384037ce9566347e0326`  
		Last Modified: Sat, 08 Nov 2025 19:22:10 GMT  
		Size: 90.9 MB (90949491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76b83a82299919f26faabb6cb6ed49e1714b0447a1bd4361da0f17870320e63`  
		Last Modified: Sat, 08 Nov 2025 19:22:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d76c700c7a4112107d92bab7ab2409faed1ebbe85dc1507fa2160a5b10057f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05eb974a5760c65dff5ea1e22986a3268bbc258ff2fbd4c6c3fa5a0815435cb0`

```dockerfile
```

-	Layers:
	-	`sha256:84bdd75d174b6941bb8e4fce29c8bdf3f2a987dd13668135fc96aa886b25519c`  
		Last Modified: Sat, 08 Nov 2025 22:55:42 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6faf60f0d2419890c4c5df9e9e221ce0906e37c0e19344f6a4625752775e4ce8`  
		Last Modified: Sat, 08 Nov 2025 22:55:43 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
