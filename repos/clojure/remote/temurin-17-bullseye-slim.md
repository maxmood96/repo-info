## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:cf06e0c0df5b01e27f30cdfe023cd64fced164a2e6be0847859167eea6b55ac7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ab30d83a9af493f776ffc31c38ef37082d60ff5e6e824522594c69d446e77f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234727529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87863dba52a7b3ce21a076f7f91ee0bce8eb28c7a6b3b257196e5c4f3569b041`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b8640f6842954e6b24865a101b7932c15c1c539a93042c0ac60da47fb4c551`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6068d4425d17eea2e05f886fcfe55943c07ab989bcaa4093af56792bec2b87`  
		Last Modified: Tue, 12 Nov 2024 02:24:21 GMT  
		Size: 58.7 MB (58740168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e774488dd10998269dee4f17fa2d0e641ce3ba769dc4b42a8d6bed56d4fb9b`  
		Last Modified: Tue, 12 Nov 2024 02:24:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f1533028777e82cec45591ae56080481b9c29b73ca69ac1a3413692f8719f5`  
		Last Modified: Tue, 12 Nov 2024 02:24:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5442794698018783053e4c089167de8218a599afd0d4bad052f066d20bd80903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53b55ba58ef0dce11253960ffd85fb9cb336860f12484a389ad232b1050c318`

```dockerfile
```

-	Layers:
	-	`sha256:7d4e41a9e6cbbc452a6027a8f9587b3b2458c8d668fc082b903328e17930d61b`  
		Last Modified: Tue, 12 Nov 2024 02:24:19 GMT  
		Size: 5.1 MB (5125352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013aaf07013a3a13cdaae738da690f5f7f8a46b5850927ad4f47c6d2c9cc7aab`  
		Last Modified: Tue, 12 Nov 2024 02:24:18 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7def7862e08087c3254d8e13a7e61df52e21797ac2d87b68f0d8db04a53f6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234734605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8210104973a049db0c05f87c7b38a619fa7a213ad416e1ec8f83a29b4fb2bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9573ebf30d84979ab9243f8719a10548944ad9e1c6626c4ec7fca113cef24304`  
		Last Modified: Thu, 24 Oct 2024 03:37:49 GMT  
		Size: 143.4 MB (143360974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c7227d8b1a4a3b2a9669566eac0ca5ae7405802f9c6d54814d77323c6d28e`  
		Last Modified: Thu, 24 Oct 2024 09:22:11 GMT  
		Size: 61.3 MB (61296836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e45ba11b41ed079b198c05e4ca2af4eda69e37997202a5c3ac3f977f0282e9`  
		Last Modified: Thu, 24 Oct 2024 09:22:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa908f4c32395c01379c1537464056e963c1ef3972927fe66cad8a3e60217fae`  
		Last Modified: Thu, 24 Oct 2024 09:22:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a42829a06f995599ca48f6512f901a7293fd8a003a5145cb0072952fc4269c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6335daae5362217326095cb55e14146bffe31dbfa072110269931eca22d2f331`

```dockerfile
```

-	Layers:
	-	`sha256:f6cfc7c8719a35aacdd0f683f22bdb059c6f0c9341566c93ba4dc9331e2bea75`  
		Last Modified: Thu, 24 Oct 2024 09:22:10 GMT  
		Size: 5.1 MB (5131053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7600fe230715455287bb253181712390e554d7d485a333c1c98fad041032318e`  
		Last Modified: Thu, 24 Oct 2024 09:22:09 GMT  
		Size: 15.8 KB (15831 bytes)  
		MIME: application/vnd.in-toto+json
