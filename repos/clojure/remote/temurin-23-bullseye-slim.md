## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:828da7081989f983faba50c12607ee048dc1634a213db8446ac20fdaae9b09e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:87da4116257e0c07733557cc399273e5d14b22737a729d5228eb7716b9f949ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254357823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4905c9d03db40562902cb64d240ced97f46f4ab5642af0906aba704fd5b7daa8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b3dd06dc3036f4d76aa5abfb4b25488149a200e75f2a9ad850d6f2e1bf353f`  
		Last Modified: Fri, 31 Jan 2025 02:18:34 GMT  
		Size: 165.3 MB (165316197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413aa09d256ea13e2bc71b141380449e6ceb11733a52d6b643dac4be8e22c47`  
		Last Modified: Fri, 31 Jan 2025 02:18:33 GMT  
		Size: 58.8 MB (58787919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535ce88420b18e06fbf1d27c11b99e37122758c86b6e36afb0dc7352ec01a5ad`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6d3d4b77900994e38630607eef527b0f5b1630fe076908544aac4a0528e53`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3617688ffce4b75151758d3040625f390dae4db7d25c625bf14df39ed6cf226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dcfe7bf887848c3af9298cfb0fae338ef55d787e0fe5bf1c97d38223553143`

```dockerfile
```

-	Layers:
	-	`sha256:0b05269dd6387ee12402fc46a75ed021f00400a9c2422099ea328b4592a76152`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 5.1 MB (5122072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101360e4db6c26c683370d601ef40c6dde24f956c0b3ffdb2d918b67a6cad5bc`  
		Last Modified: Fri, 31 Jan 2025 02:18:32 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ae2f4ed97c1479177315ad8011be967a2965f1feced8fe45132118056562a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250996327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a799e9fd6c7ab4e07dcce1fdd7ff820f2065aa4203756c503668c52cc9bcd2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb526c5d9257b008ce9e6f38b15ff60d85e230a9348d9b3dfd8794b4a0feb10`  
		Last Modified: Fri, 31 Jan 2025 05:31:53 GMT  
		Size: 163.3 MB (163341446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695d689ef1ed51c811a1d75f1c03bbb24dd3231f6c5b86e7d91bd5594cf9a92`  
		Last Modified: Fri, 31 Jan 2025 05:35:44 GMT  
		Size: 58.9 MB (58908926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb7d57d70f3629375489d375cb04ca5fb569e11272ef60e44f3a4ccee6c0e36`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008c0111ce523ea7095c41b55e66248605a76a180fe39b6e7a0dc68e3dd0739b`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74aa87bd8e8da96ca6efcd86a696417de9fd366b9fbee946911bbb056439a6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be38960fe9007ca4c621bdff6f7f5378bb20035eac1a5d3f773afaa4cadd8228`

```dockerfile
```

-	Layers:
	-	`sha256:4b9bacbeb743493f509e890b49d2b3fbafa5231f6f3df57f070fbc449d592677`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 5.1 MB (5127183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1ed2f8cb3d6e65fc1782169b6667e62572574f2fd28552024f206652c0f65e`  
		Last Modified: Fri, 31 Jan 2025 05:35:42 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
