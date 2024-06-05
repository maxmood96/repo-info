## `clojure:temurin-22-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:178d407106c1d798921877e5cc86c904100cf9ad1a9de759aa551d2100b4a284
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5099aa52770ac8bb8181e4a4ae2cfeee513170e30cb5d96a74bdb9cffb7252f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286592743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5902cdf715b4e9e383e9717ef483261fda9fe82b20219377fd62b6cdcd79b48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1be7480ff186bf4401710829ce4127dec1b7668bff4ba09be1c74544c46961`  
		Last Modified: Wed, 05 Jun 2024 06:12:43 GMT  
		Size: 156.7 MB (156715500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebda725f227678a9f452c738618d42700abec6ae13d4f9c2a7fde3e6b020a42`  
		Last Modified: Wed, 05 Jun 2024 06:12:41 GMT  
		Size: 80.3 MB (80299808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54666769fac3162d9486fcc2cccbfa0ab85f1a2cc27a7575caa5f4e9442fab6c`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a60b530aeb5f252b8bfc0b1ef127149100ad63d483f5f4357570c773c8fc035`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:78af58fd60bbb76261c641147fc48cbade8b026ab2874aebaba0f91f7fff383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6977418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b825970191bd8abc7655d81a54ad441189d9ea91502c810b03e14606a5e807b5`

```dockerfile
```

-	Layers:
	-	`sha256:3c1c7b51c8c630fd511939512b9ba5d17cbc60cad1d415922ffd431d2c7656bb`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 7.0 MB (6961344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:521010bba5a66b6edfbb63d7ce14b083a1f37cbb6c6ceae409cf96307c2735aa`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 16.1 KB (16074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d69d5b7c12eed87e26219eed326bb20f57765d8447d2bf9b47d0b63f0624d3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284397670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b801bfe7f75331b22768ef3fce6ccf9f5d68f953782c9930b24448142af374e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0d24da5c52d29fa2526287f370f8a6d73c90a9548b231bf51c7055948dce0b`  
		Last Modified: Wed, 05 Jun 2024 14:19:35 GMT  
		Size: 154.7 MB (154738035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc640ff4266ff7d2b5fa84e84d857c47534599a72c8688362c72ba6cee6c270e`  
		Last Modified: Wed, 05 Jun 2024 14:23:55 GMT  
		Size: 80.0 MB (80045198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224522f0afedaaff857645e590a9a1317569d2583fb433d0485f5d1a1704602e`  
		Last Modified: Wed, 05 Jun 2024 14:23:53 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4d9b4200e0281eb33c16bcf29e02812e57cef072dc9f2e62d18332058a365`  
		Last Modified: Wed, 05 Jun 2024 14:23:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68edefed774f2c848d765527bc40ef4d5d55c7e8b825acbfb59194eedfac6a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a2cfed38398a8d02d975070d964164a99d3d810c3794c67b1aaadb4e663bc8`

```dockerfile
```

-	Layers:
	-	`sha256:4593654243fec763112fe8250268fe339df8be28863ecf19e4db1b59d0e8bea9`  
		Last Modified: Wed, 05 Jun 2024 14:23:53 GMT  
		Size: 7.0 MB (6967755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e2f5e2a0ca50ddf50127c918e50d1bec9b9a8d21c3c1bd6c572b6652a3c5661`  
		Last Modified: Wed, 05 Jun 2024 14:23:53 GMT  
		Size: 16.6 KB (16634 bytes)  
		MIME: application/vnd.in-toto+json
