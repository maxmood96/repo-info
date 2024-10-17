## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:e635893f7df28a29b77089a675f493d091146f5dfe896d9cac2d489dfd8b4d5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ea0007f677b4e4f4b0c5db5e36c0350a9ed37d8f22f202ffe27f23fa71598317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295751716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e1e55856d40c9733e2eda088ed455bf565f0f5f80f165b8f07b3e51db90ddb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68f122a48350ce95e50896724eca961fdb8235429755ef94bb4ebd2a551d57e`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 165.3 MB (165267630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2feb92f830c4f1b10ecde3eb2a6bd9cb1b7955aaf4af651aec01d79e6c525df`  
		Last Modified: Thu, 17 Oct 2024 01:13:47 GMT  
		Size: 80.9 MB (80928024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94580c18e453d533a6df4758784eaa7be5cd32876b4556b30ba4d2e1555c4779`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee7475e678dd4a576d64a8f1ab5c4dba1c5510825e941722fa37fadf62b6d7b`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:79406cfdb0f0f038a0bf1e3739b29ce20089560ec47debf08a87b3dbdb12b73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6593fa6f233f79afa42f92dfb8f8566c65a17e58335b0ed8305d7819250e3f`

```dockerfile
```

-	Layers:
	-	`sha256:560410e180e9064b2cace656bc5075276de700650adde16a7c46c2b778eeea6f`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 7.2 MB (7162323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46800432b824bd30cfdf15c5c7511c39483fd3295c2881dfc399170570254fb9`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-23-bookworm` - unknown; unknown

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
