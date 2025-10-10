## `clojure:temurin-25-tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:d132505351f8070cf6fd82b64ae6ac75bcd7a285fd63854f9c5eaeea209086e5
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

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; amd64

```console
$ docker pull clojure@sha256:5c5a3466fb84c8fe55b1e605923c2d1db148eae3f327a7b52071a185ddbe9f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221664456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d62c80e4deef4ed89582ff8f0e266730e861e204dbbd8e8263917b12f59ed3`
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3164c425ae23e58663cb79dec6a1df7b9db5f64e0580288a09fd7876291ea775`  
		Last Modified: Thu, 02 Oct 2025 12:59:24 GMT  
		Size: 92.0 MB (92036038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c49db35dfe7795e75e75867534515b3a796d669d3779bae90af3c9c4b771ec`  
		Last Modified: Thu, 02 Oct 2025 09:01:49 GMT  
		Size: 81.1 MB (81146819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91dfc599d54994e08a4bf4f99c531854d466db7b1f1d3277e2e6f0ade84bb3b`  
		Last Modified: Thu, 02 Oct 2025 09:01:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe318c847dc9870cbff34ef9ebe2a9f03f772e5b0941e67c8f2d0fc4115a7ede`  
		Last Modified: Thu, 02 Oct 2025 09:01:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:9b5fd9cbaf780fd8ded83c945f8477c48b33b6943cf11ce2caec9dbdb7b2a484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48d99a49742c4454dbf19d93f8cf92660b100c79893936227e95ed72ccf5d65`

```dockerfile
```

-	Layers:
	-	`sha256:ea45981ace8f01292196789b77bd04841eb2273da73f9d971f5534cf76c7491a`  
		Last Modified: Thu, 02 Oct 2025 12:43:54 GMT  
		Size: 7.3 MB (7327540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f19ac5bfad4c822222f42a98b768b331580423b8ea9c6738d8516b47b43fccf`  
		Last Modified: Thu, 02 Oct 2025 12:43:55 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20c26c25a54707b67b4d777b04af330e5c9043884408b2244c942485381b3a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220435309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eedd1a5b1b18827970ad45745e082fcd882598273b69a6815aa68613956c4af`
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
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016a4f8c311b02797ff30d6e17f51693e692d66611f741514297e5e9f52fbf04`  
		Last Modified: Thu, 02 Oct 2025 02:47:19 GMT  
		Size: 91.0 MB (91045294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33964f0a205a7e3a2e2407362ccddf2f6ef9cba160fb4869bd34f6bdf852c97c`  
		Last Modified: Thu, 02 Oct 2025 02:47:18 GMT  
		Size: 81.0 MB (81030063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fae51abf05c7a2ab1a747c5a67665e0050c9d19b31606dd77775ff9ea2c807`  
		Last Modified: Thu, 02 Oct 2025 02:47:13 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aa9f31d3492bfa5175f87768d93b54e47c96e82197c12c3ed6035028290d14`  
		Last Modified: Thu, 02 Oct 2025 02:47:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:51491d1124a20918e6b8c268c85aafac2f10ac69d65c02b429bca22adc1c6f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b563ca8cb3d65c68dd6b8ecb69571ca811ecb9e8ce2a5b643987c1b838c6ab0`

```dockerfile
```

-	Layers:
	-	`sha256:e8a93e62256e59ee3f02d239dda38e47e5b929ffe02a8a08ce7b05e7c2afee74`  
		Last Modified: Thu, 02 Oct 2025 06:45:58 GMT  
		Size: 7.3 MB (7333372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bab786035f0cdbbcc9a67d2a522d27b0ee545b6c7ede6f514f56fcea1e84194f`  
		Last Modified: Thu, 02 Oct 2025 06:45:59 GMT  
		Size: 18.0 KB (18004 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; ppc64le

```console
$ docker pull clojure@sha256:0feb2c40156809a93138797062a732fd10f0f0eae48f1925437d6c32febff0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230915541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9199296807aeba8c5614804da52e2d5a4403584cee84c6eb0153c5608c0bc19`
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
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690631a1d691440672f0cf2bcbd6ec4378a12724c4524e3fae944324ac8291dd`  
		Last Modified: Thu, 02 Oct 2025 07:57:16 GMT  
		Size: 91.6 MB (91601759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf37658d4b95ec8457f3c17a41032de7891e2a459c2abc757a838e290ee6cec`  
		Last Modified: Thu, 02 Oct 2025 09:39:08 GMT  
		Size: 87.0 MB (86985979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bb390790dee2aabe7727174a1051f8e7e52287db14f0d5307c43957a2a0749`  
		Last Modified: Thu, 02 Oct 2025 09:39:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3669993717ddac5bd8301d8a9f6f60a47d987b829c551b9a754e1fe1946ec1d`  
		Last Modified: Thu, 02 Oct 2025 09:39:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:583fcdc7d0576d1446a2ffb757dc1b86a61e1b0e0c330fc4ef08955b4440be88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00652bfc73667a5222eb7a1448a04587da106097ba02fd06065db1c081b4c4db`

```dockerfile
```

-	Layers:
	-	`sha256:a490187a3610f49df0ceee6ff46854234226e72f4c8825b3854d3665ce54a576`  
		Last Modified: Thu, 02 Oct 2025 12:44:07 GMT  
		Size: 7.3 MB (7334088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9030ec3eb4d799eacb8dbc55727be75a8d199353e81b45366f028931315562e0`  
		Last Modified: Thu, 02 Oct 2025 12:44:08 GMT  
		Size: 17.9 KB (17898 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; s390x

```console
$ docker pull clojure@sha256:7cdea8ce5e0fb71158d3e82d1e3b334a885c0926973af26ed703f8c1235c0a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215301482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be078a1b328a558ad40cb44065f915191d061d0b33dc1de536f73c8e582810`
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
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0377f9dba375d95cb49de92a8238c46c38f8e06ec3ab5ee54df5d9cfa7d596c`  
		Last Modified: Thu, 09 Oct 2025 22:50:23 GMT  
		Size: 88.2 MB (88206454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1fb9b24eb065263bfd38a77e2470fa119fe8a09b6f0b9c9beddb6ec4dac202`  
		Last Modified: Thu, 09 Oct 2025 23:48:14 GMT  
		Size: 80.0 MB (79956540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b358ed68a3b042151841e6cbac166dbfeeaa8deb52027ef1272eac0694edaad8`  
		Last Modified: Thu, 09 Oct 2025 23:48:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac325d0149e2edadb82ff50baede78095e93c062db945bf7ac6c21ef351753f`  
		Last Modified: Thu, 09 Oct 2025 23:48:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:1a6ed07403cc8793efcabc05221bfec140f55206d57c7381f8912f65d94dc36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4ba977d5c9a8cec195525b61c7080a534508e81fb28511b811c8ba94ec9510`

```dockerfile
```

-	Layers:
	-	`sha256:b942cb2afde237e834f8b26760a600eaa19f65f267ba9b03bf22d070d4a0c9b1`  
		Last Modified: Fri, 10 Oct 2025 03:38:43 GMT  
		Size: 7.3 MB (7321407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338cbd53899ef9f68230e32d6c084e667e22d81e5c15d43a66083f602dfe437e`  
		Last Modified: Fri, 10 Oct 2025 03:38:44 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json
