## `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm`

```console
$ docker pull clojure@sha256:95f60bd425d90f52399c49e432ac072bacb72846edd65668db12587b591e0cd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:37e5c76290fb2a21045e6c7f2d9c11ec2e46b41ab9ad088e5e765bb64ee40da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275072904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bdea3e9a6eff0819ff559b4fe986d33ec631e2fa38ba432fe1139c39eb67da`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cc193035872b7d7860a819648b37043a18906f6891b49ccfe864a9d2fb3383`  
		Last Modified: Tue, 04 Feb 2025 05:28:23 GMT  
		Size: 145.6 MB (145598914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36846a07763a309d191dd475e67c22f440b3171d90ad048092f577e4e185bf6`  
		Last Modified: Tue, 04 Feb 2025 05:28:20 GMT  
		Size: 81.0 MB (80993661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e39deaaecfb8fc80d9ce823ff6c3656c5b75e9f8679324d608166fca08f998`  
		Last Modified: Tue, 04 Feb 2025 05:28:18 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8d1f9fc0bb30dc1272edc39f1cab0c0f6d4fdfa212bb9714286d33f296f95ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfc71cc1960504e7e894ba80e6de1e64f0f72d44ecf57d6b90e8d07b202e319`

```dockerfile
```

-	Layers:
	-	`sha256:30cfebb15629da431fa64b1c55ff801100939629b375310f4d9a2a14a40b0daa`  
		Last Modified: Tue, 04 Feb 2025 05:28:18 GMT  
		Size: 7.2 MB (7191219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ccb48f7ac212b2be6fce430013b179bb432087861a4a83cdb083a771b59c8de`  
		Last Modified: Tue, 04 Feb 2025 05:28:18 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a5313cf1a3e2106607554c55a49accaad7e1d516aeb174a0347c37ed1ab38d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271538649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ca83d94579d4dd4eed5c6df9ed9289abec7d8066733fecdbf3799790d66ed3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da991aeb9179874ea9db6574a6a0f7e557d853cc6a751ebb20b9e551b36a8c76`  
		Last Modified: Fri, 31 Jan 2025 05:01:08 GMT  
		Size: 142.4 MB (142385531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5538dbfb2293faa525d93117aea9350c641ac4af5185eb47afb3947ae6a0404`  
		Last Modified: Fri, 31 Jan 2025 05:05:45 GMT  
		Size: 80.8 MB (80845576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623567aaaec3dc3aa7c838cf3eb6a3b41db6d3de2e12336d2cd9c5fea1f5dfe`  
		Last Modified: Fri, 31 Jan 2025 05:05:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2887c56a4253b13a296c01b9f9ce19e5975d502bb6c1e1c7d71f47efdb400ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261c48bce94cbcd29c5969b29db1ce842e530548fbd66133462f4105651397c2`

```dockerfile
```

-	Layers:
	-	`sha256:d585de443130b667d6595d9abe0a92406c43d040276144d894ff3d27074b2cb8`  
		Last Modified: Fri, 31 Jan 2025 05:05:43 GMT  
		Size: 7.2 MB (7197600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5ce6d71d60daad4bf72f8419ef996ee36902b6f40e2ee6e4041f6dbcf13768`  
		Last Modified: Fri, 31 Jan 2025 05:05:43 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
