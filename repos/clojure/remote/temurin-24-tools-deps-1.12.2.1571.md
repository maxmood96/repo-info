## `clojure:temurin-24-tools-deps-1.12.2.1571`

```console
$ docker pull clojure@sha256:51b2b889f3b647cd1283785e62871fda1ada4bf82be61b8e4f7f6503e3319221
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

### `clojure:temurin-24-tools-deps-1.12.2.1571` - linux; amd64

```console
$ docker pull clojure@sha256:3fe27c7593e35226d0fcce48475ae5e8a63e2243c031d262e178d17aa9f62ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219597895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc72ded8be6d86ff1713dca9c7c04e0470d3723df7e93eba65702b3b071f9b7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68e78b0e3ecccdae4e44bd6f6f2798f6284db9184cd410625bfcb9d278700e6`  
		Last Modified: Mon, 22 Sep 2025 23:46:38 GMT  
		Size: 90.0 MB (89975264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cc8162ce5b5b0b6868f46ccc48deb2d8b743fe28efb242940d733f05be8fa6`  
		Last Modified: Mon, 22 Sep 2025 23:47:02 GMT  
		Size: 81.1 MB (81140976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3433b2272076e287dc4b151582f504599169531979a474b07baaf118cda2fa02`  
		Last Modified: Mon, 22 Sep 2025 23:46:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26271dff6366d5edb7cb192cf23b3665bb3be5533d1c51a287ebd815b444630b`  
		Last Modified: Mon, 22 Sep 2025 23:46:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:0fd30b1bde38c793ef40a3bf72d01e786132464e44cac4ff5e52f6ef755569c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f47588348e58dcc742bd2043a71d090224444038239bef0369fd9578a5862d`

```dockerfile
```

-	Layers:
	-	`sha256:d8708031d9000c6fb85c2b94d219fba9cbcdeea1481de6cdf58cdd55e5126323`  
		Last Modified: Tue, 23 Sep 2025 00:43:53 GMT  
		Size: 7.3 MB (7326222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140c379344ad467012ce01ce8b8a06130ab49fe154107f895ea5d639c5977383`  
		Last Modified: Tue, 23 Sep 2025 00:43:54 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e65ac0f49c4df36f1234e535e0dded836b34af663d1e1d84c832cd6bfe8488d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218483721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f830bb4f49f635a1bd6620ab67b7dd0a43375417c9e666431ddb34e7cb63fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce080473d50a223a14fadab04249ed38a2d1fbbd7ed2a80d7a5bf982a64d32`  
		Last Modified: Mon, 22 Sep 2025 22:21:02 GMT  
		Size: 89.1 MB (89092524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d133c7bac5335ef90c7335acf63443e4f59b763dd52083c63648f8379cfec72c`  
		Last Modified: Mon, 22 Sep 2025 22:21:02 GMT  
		Size: 81.0 MB (81031134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe7c1e066cd2f9ead06b1c251dce15290ab748f624e153bfc1a450b92fb279`  
		Last Modified: Mon, 22 Sep 2025 22:20:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc6d88704ffd23383198ed81b123f4832dba3c5613631dad9600ef8e23a60a8`  
		Last Modified: Mon, 22 Sep 2025 22:20:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:1354cbc5c52781b9e62bfb3d40c32e7096b20e843096b11eb464dda030eca3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c43538ec8c303268b4e2c0738ab7250ed7c44305c4722a8fff78b8b8143932`

```dockerfile
```

-	Layers:
	-	`sha256:b8550034514d2275c60a421e2813244bca4b8ff08dcf590676d75fd1ae673a5c`  
		Last Modified: Tue, 23 Sep 2025 00:44:00 GMT  
		Size: 7.3 MB (7332006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8342af15312a906271342387c46539cb39bd3c9cec7f470b18d0d6ec43a3c8b8`  
		Last Modified: Tue, 23 Sep 2025 00:44:02 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571` - linux; ppc64le

```console
$ docker pull clojure@sha256:857bff058f44c2259391dfa424c377201b8b41d66a97716bd08edc4a4a80fd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229229362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14386543505cf7aa61525a902e9721f35b56ffe25e0ff9ba89d4c17468f3044a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86172f15372b948e9acf8523414dcea949da4bf6c2e68bc45159e62ddfee9e65`  
		Last Modified: Sat, 13 Sep 2025 03:50:01 GMT  
		Size: 89.9 MB (89918193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de47c6d9104e13658fc44947a1e9993afbe7554679b9d439ab5d910950b5b17`  
		Last Modified: Mon, 22 Sep 2025 23:23:01 GMT  
		Size: 87.0 MB (86983302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14548e14c7739c664b468cb72930e622c29007381fc97fe8b5d7e8bcd216f320`  
		Last Modified: Mon, 22 Sep 2025 23:22:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c850503bf4476806cba499a95cf560090d9c50ef53d943d7dce54d84cf3188`  
		Last Modified: Mon, 22 Sep 2025 23:22:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:dfcc91d555c24c2d37370205b372c17c36c92735bdb07d38d3144abd3737140f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7349304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2ade6f2d1a205a83fae423f0f58096e9f8645ace54793d7bb73e2fc5c73b6`

```dockerfile
```

-	Layers:
	-	`sha256:757d939dfca0dbf630c5eb069051a6c9b07380c80f69651fd798daab227ce823`  
		Last Modified: Tue, 23 Sep 2025 00:44:08 GMT  
		Size: 7.3 MB (7332746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b3e50b91c84a3d86a2e3aaed6fe07a364ad3a2469240e7dad0a3f1b728b3c2`  
		Last Modified: Tue, 23 Sep 2025 00:44:09 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571` - linux; s390x

```console
$ docker pull clojure@sha256:3618d455d88c231d5b8f4749ccf574f8729b08e9fd82590422494d7d433b90c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212322765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01c02005e755b6d2648ed03125875095e7ed561e8fe731a07c6642e7f7e0e69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a194a3e86b38170126e14a8a4967e24dd619d46e1914dcccc96f552585ef697`  
		Last Modified: Sat, 13 Sep 2025 00:02:32 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20dc0b8746a04d7920eebe496df39ae8ba76d0916a02e37781c8e60da7e5a0e`  
		Last Modified: Mon, 22 Sep 2025 23:19:40 GMT  
		Size: 80.0 MB (79957773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef3e4cede826bfa449950df8e1cfd0fcd60c77dbc015051bb84c37019dbfeb`  
		Last Modified: Mon, 22 Sep 2025 23:19:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f210e2cf7d819daab6a50ef650f4034057e86c4d1f10c3a6660b764540ec5d2b`  
		Last Modified: Mon, 22 Sep 2025 23:19:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:11f8bd5c3ebd096617a16d06d9036befd29749898ca9922a27e278b6ac6d3e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1200270026919f86917f06cae613882f8b6312351fbbbb765d41111672c4dbe3`

```dockerfile
```

-	Layers:
	-	`sha256:d95b516523bf3d9efaeed5799deeea576ad54fd918353541e8a1ea052d4f8823`  
		Last Modified: Tue, 23 Sep 2025 00:44:14 GMT  
		Size: 7.3 MB (7320089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:358ee6b1ba4a0896127e020e21156ef81ce3d6dacdd2213c63336225ef7d8fa7`  
		Last Modified: Tue, 23 Sep 2025 00:44:15 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json
