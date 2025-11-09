## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:0d41bb81a48ce0aa551a8f7df701e541bdbaa29961a0447e71f5fa9a6743ef7d
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3293fc4ea268fee937c88a6fc5ba8de9897240902e6a142295874c4266cb78c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242875218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d9d978c244bb6ced299816fe60e879c9fa118d4136f604490f761f54e65ffc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:41:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:35 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:35 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b81d1bbef80f4319ee834db1a886ed84c9fd5025d2590804b5478bc570276`  
		Last Modified: Sun, 09 Nov 2025 03:11:41 GMT  
		Size: 145.0 MB (144966518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdc08a7c55903152dfeec105de72670742bbc89ca9ea07f32c6bc5fd83bfeae`  
		Last Modified: Sat, 08 Nov 2025 18:42:37 GMT  
		Size: 69.7 MB (69679489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba6e7b0bec71f8b9468cdc980333df41ee6e5824f4ca32fb005e01f73c4e7e1`  
		Last Modified: Sat, 08 Nov 2025 18:42:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4978b015a73d562a091255bc4eb2dc0a69156170eb6a25620132bb4e349a1bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f9e8da249b1564476e339cf9439e6347bf59c3769278f0249999554a131e66`

```dockerfile
```

-	Layers:
	-	`sha256:ff2bec5e664b64e0d150665871d6c8c18f4b6cb78dcacb48037fbf681f2ef1ce`  
		Last Modified: Sat, 08 Nov 2025 22:36:30 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13576f26ef51dd528c11ccbd8e87e85c05e619333f6aa99927a594795271fd4`  
		Last Modified: Sat, 08 Nov 2025 22:36:31 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f07856af4c2ca0ea405b9a495ff71e229f7fd7309cb31ad8acb8cec382e62d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239395015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a167c2cc312b87f7aa95c1b1be9e264e8ce06e14ab132ecdfe855b67c462d0b9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:41:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:15 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8558ac1f7552d2427429eb8b9bd48fc62693640996ef9670f0776799a9e3a4`  
		Last Modified: Sat, 08 Nov 2025 18:41:53 GMT  
		Size: 141.7 MB (141731669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f981ef434cda2e6260f7b427d64aab4fcc9eb3ee8c7336f3c759c3dbef196a67`  
		Last Modified: Sat, 08 Nov 2025 18:42:30 GMT  
		Size: 69.6 MB (69560328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a68810cd95f68c686cba04ee06c671deee86dce9b31f92d81ddabf4d829b6b6`  
		Last Modified: Sat, 08 Nov 2025 18:42:25 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5f769f18eb2fb1ae8cf3e60487050c5f2a4158da0b15f732c71cbb8518e2c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3622818d5711f087061fd304909e63a88cadc594a6c0d03c3678ef58ae9d45`

```dockerfile
```

-	Layers:
	-	`sha256:0110a72daa008eec6a9dd1924832312e19a20f882af5a908841f72772f84f7b1`  
		Last Modified: Sat, 08 Nov 2025 22:36:36 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0c0b188ab38f7a3e6de5289836c1e91c7e169c044ee316b3a2aaef469ebf1e`  
		Last Modified: Sat, 08 Nov 2025 22:36:37 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2c862fad9086c5da5f3d4017774e20587cd4d1d51f21ef7504b5d1f3eff160c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239662629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fa07abd6fb73127730533bfb740a4dd9bd8c03635a0fc28510641ca8b78988`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:25:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:25:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:25:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:25:14 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:32:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:33:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:33:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7cbe3d3d06402157351db4258906cf4ebdb1660eca1058f05eeb89ae2d1a3`  
		Last Modified: Sat, 08 Nov 2025 19:26:26 GMT  
		Size: 132.1 MB (132079869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d1e6b4d91e9cab920ead52c4cd809e0223e7bdd89b36d548fc2707e33dee84`  
		Last Modified: Sat, 08 Nov 2025 19:33:46 GMT  
		Size: 75.5 MB (75513210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b91340fcdcd7064ed67f53478cc621aa7be057fe89b291bdba30a23b39990`  
		Last Modified: Sat, 08 Nov 2025 19:33:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddf61d68cffc8855e42b1e270c8912f3ccac2514e5c2b6e25fcbb9cfd63fd578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2728a5ce96e3907323aa71441005fe3bea28b96dad66183bd427c1fdcdcff`

```dockerfile
```

-	Layers:
	-	`sha256:4d3930f10e3a67d03bb143e981bc6afd35454440a2cf5ac712144cd3caba2923`  
		Last Modified: Sat, 08 Nov 2025 22:36:45 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ecfe0676ab0543297898ed8b45985e69e12825332d7b7899791dcb9233494f`  
		Last Modified: Sat, 08 Nov 2025 22:36:46 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:634b5381cbcf5698b93ced481289e35d6e31ecf81720262031bb4521baa8d056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221070165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15981e78e49c9b6f2355035fba02f35b80e950f4032560274a76e9fdd96312f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:25:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:25:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:25:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:25:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:25:21 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:31:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:31:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:31:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a689bd0fb689736c8baf5428bf0c0e257457cf34eaa52365761799bdaca5eacb`  
		Last Modified: Sat, 08 Nov 2025 19:26:17 GMT  
		Size: 125.7 MB (125694390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e557d8b727b7a28280a83e74a54f297422c106cbfb5659874f657cedacb83d94`  
		Last Modified: Sat, 08 Nov 2025 19:31:46 GMT  
		Size: 68.5 MB (68490581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bbc3a88faf50780555b58f484ccbca559cacae320beb9990a30a1d9e024d81`  
		Last Modified: Sat, 08 Nov 2025 19:31:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aba92343ca4911dbbd5a53a2afc30dc8a1c0299a938ccaecd6b9829655b487c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c59c73f283988d8423aa989ab9102cdbc654d344b1e1639cc760e1a05fe7f9`

```dockerfile
```

-	Layers:
	-	`sha256:dabb2d98d348a5cb10521cce9c17c1e11024558ea16b56f119344d7c147c82a1`  
		Last Modified: Sat, 08 Nov 2025 22:36:50 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5331f4f8f07f6a92d3b879ed696df4d7f201232cc88dbb46d1c110165518f23e`  
		Last Modified: Sat, 08 Nov 2025 22:36:51 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
