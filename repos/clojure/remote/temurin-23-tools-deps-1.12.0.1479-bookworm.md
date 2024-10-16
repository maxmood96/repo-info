## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:6b1d83bedb1b7bf0fe599224e9767952c38ec17cd566bf36db08b533057a4564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cad3b8ab15b8e9e5eabaedb645ee77fcaaa809177669ed4ce8b52aa21b5099c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295752013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2180353ec29505991e28a25ed4869cb22f9d804c2c8f117286f98eca135b2c54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc01e661da294e1924c9e5d41344bc4e1f3a95fe2b2c71726f44a5fa6c33a4d`  
		Last Modified: Wed, 16 Oct 2024 16:14:38 GMT  
		Size: 165.3 MB (165267628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffcd27b0b73451505f394115ea136b8464c93ee95b7cffdb346040a6c831c50`  
		Last Modified: Wed, 16 Oct 2024 16:14:36 GMT  
		Size: 80.9 MB (80928289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0e0b0632b36e0b75dbdc1c2145d3b05f6624806f423ef75db2719d332a88e8`  
		Last Modified: Wed, 16 Oct 2024 16:14:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f5ba07e931033e0d4b4d5e6c6a0cb88568aebb8b691e35924db92701e48008`  
		Last Modified: Wed, 16 Oct 2024 16:14:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:90f03c948b9af74ba48e9839eff7a3935dd384590957891eb2e32ec3358b2377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5f890fd136a1ce177f59a12818916f2ae7800208bf61d57bd87507e7c4228f`

```dockerfile
```

-	Layers:
	-	`sha256:b09c58f8b9906c21ef7c2842e7617864168ffa569b31ce413e8a7f57a4eea9c8`  
		Last Modified: Wed, 16 Oct 2024 16:14:35 GMT  
		Size: 7.2 MB (7162323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c7144612de4ff8eb154f729732baccf052920b8598e37b66457114a5d83731`  
		Last Modified: Wed, 16 Oct 2024 16:14:34 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a1f392460937f24281b93ac354bcdc74afd70a7782ef5fb0b340ecd6b9121a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293628971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1ea793df98af0bb7cf627f1804ff3b70dfc3c128391ea384add6dfe538d35e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea307bb808ed57973f55839d929bfda475e38da3d9f61a1c10f9c604e1e68a2`  
		Last Modified: Sat, 12 Oct 2024 01:31:46 GMT  
		Size: 163.3 MB (163252850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c07a9281530516c429e4e15a936c3726f53cd978f91385aa24986bd7cca3bba`  
		Last Modified: Sat, 12 Oct 2024 01:37:00 GMT  
		Size: 80.8 MB (80790192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419ce0979b181d9020bdb40fe35d68439308e58178438d2de565ba76f2a161d4`  
		Last Modified: Sat, 12 Oct 2024 01:36:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a0025c7e0b2cc828ab66cff4b7f4c124ea080e2c48dd3a4bc62985501c8ca4`  
		Last Modified: Sat, 12 Oct 2024 01:36:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4186f0f3b76c413d872a815f981564ff4c69242cf734d5434704dda724068e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d64c47a7aea99a13bd472fd3005645b2e856859d77cc3872bf70e606ec1643`

```dockerfile
```

-	Layers:
	-	`sha256:be735af3854283ceba8b25612e7f8ba684340860450af6addfbb1bc3c7e43154`  
		Last Modified: Wed, 16 Oct 2024 02:41:44 GMT  
		Size: 7.2 MB (7167493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232bdaf94cb9b52d6ea8eda7e43069195a09e89410295946fdbc68e48299ebc9`  
		Last Modified: Wed, 16 Oct 2024 02:41:43 GMT  
		Size: 16.3 KB (16292 bytes)  
		MIME: application/vnd.in-toto+json
