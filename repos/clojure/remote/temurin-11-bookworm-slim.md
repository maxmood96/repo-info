## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:9cbd6f5c39ed8740b50e9d332678f9f091137b1ad42a1bd93095ccf6b18f5e54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b0ec3041ec2b533fe26d8801b6e96fd822308f57c070a611863e705b32f6f631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243524793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e001232498fa814087fa81af7b1f08437fa467cecd2c7caae336c773e2c70d8b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173559f4941d0f6fd9dad904f826952192d6d4459cfee940b5cd84cc874c8df9`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 145.5 MB (145505194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a88b4981143314111492cabe5ed8f4f5244fa6fee5dfc6ff68838ba36e2201`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 68.9 MB (68868540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81540a573c92ee758fdc55b69927e509ac5b146979a23a9885ccabc21581b3`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35c5bbd832b83f9deb041d2648cf8f5363494d05c65456d618e6014fd4094709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc2eeeeabbbe6f5f8ef4246ef03c9183fa9f1b66a829d7376d87b0819ab29b`

```dockerfile
```

-	Layers:
	-	`sha256:343b4604871618d5bc3edfcd1e515168dd82b9286725ae404ba8cf1bfdf1f35a`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 4.7 MB (4704938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd48f0c5237cd8a6957624c66c2493fbdce752e7e0aba1e88cd2e13da70bdb03`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c30c8414fefa0751e0a444aa43d3ab940e2149e5625ab18f6574890bdcb0f36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240105078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a088543a51dc4705c05ad1c802d9909aa24ae065e4c21ba71092edf342816ec1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4da0edc1758d81eb3c66f753c37cc4200c2b16f103c1e9223f076a2621e0a63`  
		Last Modified: Thu, 13 Jun 2024 11:29:10 GMT  
		Size: 142.3 MB (142304075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a264ca04c6dd046d06b0468b02d90bfbc10c47af61da5a378aa60ef237916`  
		Last Modified: Thu, 13 Jun 2024 11:32:53 GMT  
		Size: 68.6 MB (68620690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01308a837d82f12997fc79287c914d39f7b8181c97d5f41d05e8c7e0e99ad53`  
		Last Modified: Thu, 13 Jun 2024 11:32:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d1cdac2f022b184d0b9f64bd25f0168cf93bd9c0df0c4bfb13d3905a9120842b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4725801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47157c037faaf44feb59db3993ee8505b405b985c6f2e15e2b9274b91832acb3`

```dockerfile
```

-	Layers:
	-	`sha256:36a5f2ab57c52abf66f8c062265edb693c021a52fe623128ef0d0987f73bff3a`  
		Last Modified: Thu, 13 Jun 2024 11:32:51 GMT  
		Size: 4.7 MB (4711323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d03b8ca34c297afc7e0ea4093e5d146cd1b2a04d14135bffcc82b961156cdf`  
		Last Modified: Thu, 13 Jun 2024 11:32:51 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
