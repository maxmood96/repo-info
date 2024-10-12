## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:5ba750101d4970c1db0ded623d6ca6a7fea5abd449d6507f0fbc87bd90b13208
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9f622a8a405f4bb2a3a83d4b6515983154218354236e3380bacd443caccebfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295751876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49433da00a8496d25350319e6dde06b0f4f34d9db99dded7b2ce7465dc5ec2b`
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
	-	`sha256:03e2101a93e17cee3361d55f61e2c6a569322289e845b8a04c648ef0679c8459`  
		Last Modified: Sat, 12 Oct 2024 00:54:07 GMT  
		Size: 165.3 MB (165267587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952e6cd42250cde04a3f0e44a8ed8dea3c512ae68e7de60ce8b167d570de0dc1`  
		Last Modified: Sat, 12 Oct 2024 00:54:10 GMT  
		Size: 80.9 MB (80928193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c40c3fc5a0fb2e47b2f8afa2d10cecda21243ebca99e100f7b7b0f4408f2ac`  
		Last Modified: Sat, 12 Oct 2024 00:54:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db537d5acfc0d18f55e7c90a0fc369f982c15aa910325aaee995b65fabce1e6e`  
		Last Modified: Sat, 12 Oct 2024 00:54:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c53e9c9906c35d93b04f48caf9d0f9a0fc612a5fbf69a21bcac9de77a82017a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f768553a7ea3eced3f7a623640912445dcc9ed0740477b61ad9e4db4766231b2`

```dockerfile
```

-	Layers:
	-	`sha256:7f4409971b9469dcfd01679c40e9742e1a46d724f94e9f7c269b5bc3c49b441e`  
		Last Modified: Sat, 12 Oct 2024 00:54:07 GMT  
		Size: 7.2 MB (7162323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6beb8addd7193e5a0766ff64609426eb5939fc3fc2a2de19c2701f57c412d18`  
		Last Modified: Sat, 12 Oct 2024 00:54:06 GMT  
		Size: 16.2 KB (16160 bytes)  
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
$ docker pull clojure@sha256:67fc8f05de975fa42d51b36121de08dc3fb21ae39c9ace75af2efcf8bd9bfbb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef20529433a10d2ca5c0e5367385cbef26ca4452eeb86e103a33e3eac473558`

```dockerfile
```

-	Layers:
	-	`sha256:866f0393277f27d83acdb4a8f9397191dfc9561792ca575bfb2052acbfe23c24`  
		Last Modified: Sat, 12 Oct 2024 01:36:59 GMT  
		Size: 7.2 MB (7167493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c594d5400a3444bb62ee468ea7e2e919c811e451e75b7c79e5cde22bb92440`  
		Last Modified: Sat, 12 Oct 2024 01:36:58 GMT  
		Size: 16.3 KB (16292 bytes)  
		MIME: application/vnd.in-toto+json
