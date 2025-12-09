## `clojure:tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:3be19ffb8cb618896fa49963a0be5f69dbf8f23ea7e2ec02304b49f2540a0c97
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

### `clojure:tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5e8c1eebb4123a6f601fccc0a021e9de201385847edc1245c8f1067bf9c68700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221674067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2529901cec3a5c26772e6b2c5a178a24a9c4183eb134e8aeb31d6ddfa4786fc5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:16:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:16:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:16:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:16:47 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:16:47 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:17:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:17:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:17:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:17:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:17:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b076a7fd25db20e8dd0da8c336b688bb9b341cac90d5e5f0f2a35e40e2af7fd5`  
		Last Modified: Tue, 18 Nov 2025 06:17:38 GMT  
		Size: 92.0 MB (92045299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92523ef9c4a6a52650e44a703df29bb970b2de8b258fab20c5226df2c9d9c975`  
		Last Modified: Tue, 18 Nov 2025 06:17:33 GMT  
		Size: 81.1 MB (81146967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc2976cc9eceaf36da4e09c6a53c24e09a43238e05fccf4c8f960d7c79b832`  
		Last Modified: Tue, 18 Nov 2025 06:17:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb580243ff92b22735555b55ec3bd4142061d4e4804626a8f983ac6a2a7f9db`  
		Last Modified: Tue, 18 Nov 2025 06:17:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:730ed10eb114314fb2a327dfc11e6edcea906738234283d1577e93c7a1b37ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b21f3c2c185d536273cd225f9a9bdf69a815043a293375d72a0847fc96c1e0`

```dockerfile
```

-	Layers:
	-	`sha256:649ca3d58cfc115c95cc6a2f36f5b167799784dc1f106543cef699e5e908c716`  
		Last Modified: Tue, 18 Nov 2025 07:47:00 GMT  
		Size: 7.3 MB (7327554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dde3c2333577ca414f6bb801e8c812f844f7f20a26f7308ac3b4fcbe1ce040c`  
		Last Modified: Tue, 18 Nov 2025 07:47:01 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20214aff380f5e9fb9f9c8d064648d6d55cf1f8d51c798ff962fa179f000472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220443523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0a2b21c235b51e4baf7ec8efee5c817c4526428e1cd727b852a7aa435cde8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:12:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:12:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:12:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:12:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:12:02 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:15:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:15:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:15:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:15:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:15:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c205f6f704aedd7b44f180f1d4fdb4baa335a7feb723463afef939f491f333`  
		Last Modified: Tue, 18 Nov 2025 05:12:53 GMT  
		Size: 91.1 MB (91052529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82783cb824a3babcce01611f1123dcc11ba47f811196f8491ca097480695d7bc`  
		Last Modified: Tue, 18 Nov 2025 05:15:30 GMT  
		Size: 81.0 MB (81030814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6556495489b346ce704ccb6a815755aae22379b14bd49af277117faa302adc78`  
		Last Modified: Tue, 18 Nov 2025 05:15:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc26c232f0d5bec11ebdb7d4d93f2c7678e09d3bf848d3554b7966c79b808e6e`  
		Last Modified: Tue, 18 Nov 2025 05:15:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5862a8b3fd1267f74a43635054685d77dcf2a2d2e2a009ff2446704b319cca46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18232bff4fda914d72d16c718a23487586f2d8bce7fe61fce2c903ce2041b76e`

```dockerfile
```

-	Layers:
	-	`sha256:2beea04d37593f4a92711accdef3ab4a87341af7b9af0710323b3fb34c9929a0`  
		Last Modified: Tue, 18 Nov 2025 07:47:08 GMT  
		Size: 7.3 MB (7333386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e2ac250434717127fa88b85b78ec98cd797a59679343067d3263a03d434068`  
		Last Modified: Tue, 18 Nov 2025 07:47:09 GMT  
		Size: 17.2 KB (17162 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ac932cc2e9c21ed1d859bfed13e641764bb2a83b65e8c4e566e6d18a73779f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230924966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a729bc6da2b1bc4f7eea8221b6bbda8f6eabdbbfef70033166601e6281747f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:34:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:34:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:34:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:34:23 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:47:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:47:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:47:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:47:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:47:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeeb5c6058bd793bb98336cf15f96291626b642ff5b9461a0723bb0f77fc9eb`  
		Last Modified: Mon, 08 Dec 2025 22:36:56 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728cefd3d0455deac8bd62c99f0e77a95c7b758e833a9ee0118c176ee69aea93`  
		Last Modified: Mon, 08 Dec 2025 22:48:32 GMT  
		Size: 87.0 MB (86986184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76666e815cf634ad7c3e9aa75a42cf2268f6ecd29a3e758cad0beeda86d625f`  
		Last Modified: Mon, 08 Dec 2025 22:48:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8d4d17d064d779c85ae98b85f977d61def5c378c617c0eb5fda82e93ad231b`  
		Last Modified: Mon, 08 Dec 2025 22:48:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bec0a3ac7cf44490408168c7a42ef3ef495358510f4a7a17a1c636b1d96cb670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bd2ff6523b824d1187a73b1c3ccc6fcf04a34048cd83716cec3a134871cd4a`

```dockerfile
```

-	Layers:
	-	`sha256:3ec861f1923fd09e9a0d7dc8ad74cacf6a2dd95db1dd027904705c5fd204f0a4`  
		Last Modified: Tue, 09 Dec 2025 01:38:49 GMT  
		Size: 7.3 MB (7334102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688292e8ea22b867d0e5a1316c09cd881f925abee9fa197eec321c6c79699fbf`  
		Last Modified: Tue, 09 Dec 2025 01:38:50 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:dbdf12a42946fef70b3b4e634096b271730742f1eec59dc183a817d5697cc455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215305819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726b3bddfc4a1dee59e4390a8967fd6c6567f8c0f89a7f38e03c66275590ea74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:32:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:32:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:32:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:32:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:32:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:32:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:32:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:32:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:32:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:32:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b56a206c240d4dea43ea32bb1d2dffd2d3b0d14474676f0c1fbf5e5d5f0443f`  
		Last Modified: Tue, 18 Nov 2025 05:33:20 GMT  
		Size: 88.2 MB (88210739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3030fe1bde9c1280aceff86bd3cd9d156953ff1c590338c64637ce38cfa06f`  
		Last Modified: Tue, 18 Nov 2025 05:33:18 GMT  
		Size: 80.0 MB (79956398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6d6c9cee79015e0905b7af7badabcacf3df8cc7e4ad5d7c044dab4d660ae19`  
		Last Modified: Tue, 18 Nov 2025 05:33:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870dd5fc65b5b46f2e357191084be3da8f9edb309db7d7fb5a176f682d4359dc`  
		Last Modified: Tue, 18 Nov 2025 05:33:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0dce99d88dad24df1d0f5bde0fabd8e86a12f5b625e51431fa196c3df8c7e19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1559c1aad49181471628ff79937b7a3292b2d9f1f5a74c8f44bfa55fffa27c36`

```dockerfile
```

-	Layers:
	-	`sha256:8ea3d1a7e8e0d530401aaefca8894da1c14e71335a85c5dd7fe121243c864adb`  
		Last Modified: Tue, 18 Nov 2025 07:47:21 GMT  
		Size: 7.3 MB (7321421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a4d8a3bf8ffb0bb035c2a33ec1588b76b1c92cdf6d1aa5e1c55b7db0822865`  
		Last Modified: Tue, 18 Nov 2025 07:47:22 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
