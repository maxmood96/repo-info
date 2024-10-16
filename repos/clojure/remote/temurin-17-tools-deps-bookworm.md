## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f362c9cbea9153cfd5390c2faa68dd374cb2067eaa74dc8df89a9122b979ca10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7b9088d5139cc693fa10eea19f705bf13a700352b79b81c29d41d9e79752cf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275650931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17601c6557accbb925c1bcfbe8bd8c411e4ce345e647842a25225c1f13c07d28`
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
	-	`sha256:52cf181b1d0025d566f20d1913a51aba09065deb2390590d7080437237b8655e`  
		Last Modified: Wed, 16 Oct 2024 16:13:14 GMT  
		Size: 145.2 MB (145166561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48e725ec26c9bf5f5b66f10a87c9ecaa85ee7dd54975bb467372a35fe18740`  
		Last Modified: Wed, 16 Oct 2024 16:13:17 GMT  
		Size: 80.9 MB (80928273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40953f1300843168f31eae1480c89cf31a6c94af6c896ec0783646dc09a7d6`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be66a3287aed8fc2953d766b574943e20be6cc87d7c1c6d0fec0b6510113451`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:03639e17dbb1c154974e8910fd247fab1417eccc28bca316c1dd6d830e8adecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7171484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1202cfa09f9de033874ebf271c96acc5933a74ede5d553643d04724abe27c08`

```dockerfile
```

-	Layers:
	-	`sha256:5f111a7b9ab95328b03301e36b02e2c9b06996f268cc5289f8738be48c2ed3df`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 7.2 MB (7156006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204997e27992f3f8b94f00942266539c406cbbb0771b2e7d11ee0296f9bb2e5c`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 15.5 KB (15478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7465c9fdeb25c89bbc12ca10e3e0cdfa6176ac6ce12710c03aada2dc29cd65f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274335554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd3280a7316122871586b1e9bcc8a3eba3f652169793039384372f54c99176f`
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
	-	`sha256:5bca83b40ab7ec8da323039a9cbeb647be6cac4a3ac25dacad9868af9c7f0627`  
		Last Modified: Wed, 16 Oct 2024 02:21:01 GMT  
		Size: 144.0 MB (143959469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0028b0131b6d7fd23b15125bccb387daded3e011033789b488ee6c60f45839b7`  
		Last Modified: Wed, 16 Oct 2024 02:27:18 GMT  
		Size: 80.8 MB (80790154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095afba910e3abea4198fe88c36db0bcc15c3c04754eadf0fb3bb38379f8287f`  
		Last Modified: Wed, 16 Oct 2024 02:27:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d4f0542aeb091dca7d8630fdf73ec557e932e69a7af8ed1174175b5291a08`  
		Last Modified: Wed, 16 Oct 2024 02:27:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d5a60869434161a3857a025973b071090e1aa1967044c0a618386e5a40d20fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7177358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113017f3fdf662672775220265ec06942dd30b2fcc27e26eeaccc4578b1ca1d`

```dockerfile
```

-	Layers:
	-	`sha256:6849c4ab3a2eecb15ca9373123228d2e6b913e2746a75d24274ec4db5a50f051`  
		Last Modified: Wed, 16 Oct 2024 02:27:15 GMT  
		Size: 7.2 MB (7161774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f6e142e2636f9695ccba38014b77269b987607dd3f8509a6fb789bf9ae71cc`  
		Last Modified: Wed, 16 Oct 2024 02:27:15 GMT  
		Size: 15.6 KB (15584 bytes)  
		MIME: application/vnd.in-toto+json
