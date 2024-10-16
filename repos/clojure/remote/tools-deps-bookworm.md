## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:bc2c316dc511f7f5f67a235650c18c2678965e7d8e145ee707fc11b5274f93a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0958fe1ede694bd9afc7804a896124b1984e8b7700f26f4dc74111e3612b8f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289063634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8cb447af979537026f5c1cf56ba79c1a11bb0bd65582551bb0c767d0f77cdc`
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
	-	`sha256:0857311c3016f7fac23f90f410a34d5ccdbcbfde2e401207693958a28e5af16c`  
		Last Modified: Wed, 16 Oct 2024 16:13:18 GMT  
		Size: 158.6 MB (158579314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5522ba3493430536db54f95fc8723fb5e7506c276f5b71151cf6296610bf2b`  
		Last Modified: Wed, 16 Oct 2024 16:13:17 GMT  
		Size: 80.9 MB (80928225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5e1c206223294d39260d8affb7fffc2ef5898a25ca7589b1a0479e937388fa`  
		Last Modified: Wed, 16 Oct 2024 16:13:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac5e7273494429847780b309ae346a5fc18848bec4bef9d4703db8a0e8f15f`  
		Last Modified: Wed, 16 Oct 2024 16:13:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3edf1d9c9de6ae6033ffa14c86b3f7e21ea50bc4a0be8d478a57268d8c5883e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7179225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6570eb84089cf160a445d0a339e1ec32e9b9cdee21c26e9afce0b0f2b69bd5`

```dockerfile
```

-	Layers:
	-	`sha256:870907b54e1120b1fa4c3bd3df7ad222bc54d129f63c59cf1e13b8d34443b566`  
		Last Modified: Wed, 16 Oct 2024 16:13:16 GMT  
		Size: 7.2 MB (7161747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6632534cf89f86513a2ef4246e004451604dfbb07d3015043f546ec761ffa9`  
		Last Modified: Wed, 16 Oct 2024 16:13:16 GMT  
		Size: 17.5 KB (17478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e1af9314632e327df2f6e79e17ff4a5f1e3285d0e1756700795e33620a46c70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def86ce18a0ffd76b253d01b3dc2d78bcf334ad4b567be648c892dd252849cf2`
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
	-	`sha256:2a21e2b47f54cf68dc71a6ca9ed705169a4d785cad9444569b57095902aa78ad`  
		Last Modified: Wed, 02 Oct 2024 05:23:18 GMT  
		Size: 156.7 MB (156746184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d042b9901153cb73ebf7334cff11ad7233bc0e1e811534fe001d8e1c5ec56759`  
		Last Modified: Sat, 12 Oct 2024 01:27:26 GMT  
		Size: 80.8 MB (80790214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ac408f14471b02639633642b15bc209c84796948047a187c0d12b743010813`  
		Last Modified: Sat, 12 Oct 2024 01:27:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381e751879bff1b697085b4233c0091dda889b3489a93a4629891e277713ffe6`  
		Last Modified: Sat, 12 Oct 2024 01:27:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:91a1d3adf13c000188b55134782919f356fbe9feb48570a4408c4158437d4d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983f43861a1040520ed70799dbe2cae30e8aa4ad403b6dd87e1ff5cfd033c153`

```dockerfile
```

-	Layers:
	-	`sha256:5f8e4e4105a0e71b0cc611e49b00b927a0a34167057d19ad29b26977e14a25a0`  
		Last Modified: Wed, 16 Oct 2024 02:35:15 GMT  
		Size: 7.2 MB (7167587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2171301c35ee2780e566adc0be0b6f82a3eee2cb68bff489d0284ea3a5fea753`  
		Last Modified: Wed, 16 Oct 2024 02:35:14 GMT  
		Size: 17.7 KB (17656 bytes)  
		MIME: application/vnd.in-toto+json
