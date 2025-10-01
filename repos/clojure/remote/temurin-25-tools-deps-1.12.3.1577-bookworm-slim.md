## `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:50e2afc0e1ea8d184c4cb9916cb6f1ea114f353aea232c0fe3473388895c6dfa
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d957ae2d7aad9069213889791b47ffe0f9fbce20ff688d1cedea95cd81786ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189945638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b596876b51c178ac90504bd7d60716496ce6532e8707ac911f6c419e719d1072`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe54c49745468a73173782ded86f5184f905cbb521eb5191843c5a0b16bb1246`  
		Last Modified: Tue, 30 Sep 2025 00:57:14 GMT  
		Size: 92.0 MB (92036029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc452bbf74d4e036cbd377644931a76f231c1e67c593d5f1028bbc6ff024787`  
		Last Modified: Tue, 30 Sep 2025 00:57:11 GMT  
		Size: 69.7 MB (69680237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38616ffc722577bda61b1de1c126c0f88cb3a870944c9393288fe375f4567302`  
		Last Modified: Tue, 30 Sep 2025 00:57:05 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ea8cd441a05f9cf1c49cb1a0d6c31251d5305a036517493b1e7945e2e269a`  
		Last Modified: Tue, 30 Sep 2025 00:57:05 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bf77017c69531df73a17cb4315801e6c49ca82b0f8c168bb27b1fe61ee07daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1d819e4f595e553c80cb63e1dc464434e7a6b575ee01781b8de3ca28c3eac3`

```dockerfile
```

-	Layers:
	-	`sha256:743eba56d45c757b9b816ca3900e97a2f2980b22320598940bf3c7bde88e2edb`  
		Last Modified: Wed, 01 Oct 2025 15:41:31 GMT  
		Size: 5.1 MB (5064734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ed2f54f66fe6592b69a5cc37132a74cd4a63d8ae59c2085b11ca34c13afc6b`  
		Last Modified: Wed, 01 Oct 2025 15:41:32 GMT  
		Size: 16.6 KB (16566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2f0a7ff8883a8920bc713abac51a5ea8169edb349dd2b7b32f822a3aed71168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188708560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c287672131ed4c3e0d6af5c6492e6b3e5676190b4ed8e0b6a7781ca6c1dfdf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b794c95e07599847081263beb7366d796b6836a0914feb3ef0870ceef0f76480`  
		Last Modified: Tue, 30 Sep 2025 00:55:17 GMT  
		Size: 91.0 MB (91045254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7838fb0f5704a2e762f9bc1f76e48d8f0ee034e71f4bb12281131ca327dff269`  
		Last Modified: Tue, 30 Sep 2025 00:55:16 GMT  
		Size: 69.6 MB (69560124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fa90ce9f55121caae7a6462548e43f5f9254a35050f6569141bae55d2ffd7`  
		Last Modified: Tue, 30 Sep 2025 01:39:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e961ec431a10545a40ef6b89840915224a45a371298bcceeb9ac082d3df96`  
		Last Modified: Tue, 30 Sep 2025 01:39:20 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83c2712a53d422883a917d357a1fd632728b75995e0ec3dddaf0a364f110e996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c51e8f5d92e2324374dc11333239f7d7b1bf1457c6648834fd496e331ff512`

```dockerfile
```

-	Layers:
	-	`sha256:9f3c82d2f1c80eda3998d2601207818d55cace2a3645199c8afda837ad69e66b`  
		Last Modified: Wed, 01 Oct 2025 21:44:38 GMT  
		Size: 5.1 MB (5070516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0361ab7af6082b90dafe1424e9b5bde644e52400082d58bb75bc85e270553a5c`  
		Last Modified: Wed, 01 Oct 2025 21:44:39 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a736b5b78bf4edb01c504d1dad2b8388b53b789519b0df06c8e82650031f2ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199184728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5b4e96ae2c222a7e704d522da313d6ea967a9e413274ae761151553917d19d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad61acb2565616a9bb33c4aa694635da9cf1d6d57a0bb9dce41eda1fa85845d7`  
		Last Modified: Tue, 30 Sep 2025 06:23:20 GMT  
		Size: 91.6 MB (91601714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde07a3f28ffec299e95af265fc237a2b951ad6d36798759725fa885ce0d1ec`  
		Last Modified: Tue, 30 Sep 2025 06:26:28 GMT  
		Size: 75.5 MB (75513275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fa8bf384faed0429ae4ef073192de0a157ab6ebddd834262e07a386dfb736`  
		Last Modified: Tue, 30 Sep 2025 06:26:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a7474bab325d1c29218c9baa5a0702cb560432ba18d60ee9a98fd84948a07f`  
		Last Modified: Tue, 30 Sep 2025 06:26:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88f478abf552674fb0f7d351a96bd015ab68a00ea54109dc815efdda117ab4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a4b312c47be3d7662c6b1f0cbbe3143806313aad638973de56449a8f7fee61`

```dockerfile
```

-	Layers:
	-	`sha256:115092b6a8ebd39f54853dc140eb7849e985ef6b7986dafbc5bcb1e403ca182b`  
		Last Modified: Wed, 01 Oct 2025 21:44:44 GMT  
		Size: 5.1 MB (5071202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c95e0dd319a93e25dacef88fc99e146e712063ed5a77580d0ee3c6caae17e04`  
		Last Modified: Wed, 01 Oct 2025 21:44:45 GMT  
		Size: 16.6 KB (16628 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:819bb5ffa0692dc6e57c696de7a606be84a9f7abb9b023153e46db3398470eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183582171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea610e2605ab8b735b89d85732ee0648ef488c8445a04d5b04a7b8c88d7aa046`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3ccfaf29b57ed73c9be34431455f598466ee2e6babaa861d16b20687b27389`  
		Last Modified: Tue, 30 Sep 2025 05:59:27 GMT  
		Size: 88.2 MB (88206411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5a6c8a5e71d7db55cdacd431f12c9e413d9763dcee9a1596e884e0fffd0993`  
		Last Modified: Tue, 30 Sep 2025 06:01:16 GMT  
		Size: 68.5 MB (68490404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9a9b320959b5bbbeb1a96492d58ce77b5a90f2f4b173b1c80ddba6fd3a4361`  
		Last Modified: Tue, 30 Sep 2025 06:01:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c400b7ec2fc9cf4e7c37e44ca05d69b35da8080ff198a3d5034fa01e97c64852`  
		Last Modified: Tue, 30 Sep 2025 06:01:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e09c063ec5941d5adb76132aa0c19aa35f2a8d1b8aec0d6ef097572b5b56352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e009af43fbdf284f60b9aa7815dd41643788221e6c73802303ff55d826e56f`

```dockerfile
```

-	Layers:
	-	`sha256:20abb24f5259a8f84ff65f70a66beb1b33ed43d75a53754f5fdc7fcabbca51ba`  
		Last Modified: Wed, 01 Oct 2025 21:44:51 GMT  
		Size: 5.1 MB (5058603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4035486907df9c2f7c13d86791d12bba6ae9e8a5dccb94068410a94a55056636`  
		Last Modified: Wed, 01 Oct 2025 21:44:51 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json
