## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:00f1e03cd1736bf4c4bcf07e0b4471cc7bca297fafdd2747af0fe5a4c46c89ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1a79c7efd02cd259b182e3cd91af5f7d2f5b3c14e16b76a5ecdee508b26ed192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233867719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b18640b5a7c5182fcee764349c041b9113405a2bfa318e66fdc555442e375`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c609c4af7fbb9d22ecea6040a9624938caa3a53268dd6351c1954282c3ed22`  
		Last Modified: Fri, 06 Sep 2024 20:58:07 GMT  
		Size: 103.6 MB (103611886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897231d0b70978ac2196484b57a2e91c0fbeb1c4a2cf19c70d7de7470a26eac5`  
		Last Modified: Fri, 06 Sep 2024 20:58:06 GMT  
		Size: 80.7 MB (80698485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f92b819eb3352e63e955b560c6cb2b5e024ca3230e854e3e9674d5cd2ad5cd`  
		Last Modified: Fri, 06 Sep 2024 20:58:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ecc59bb1cefb336ed89b961bce0912666a88ec04d3e84fab0cd03235e56a032c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7038814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197a2772b0c8a818fefc64397154882f30121efc1d64795e8fcdd482fe01db51`

```dockerfile
```

-	Layers:
	-	`sha256:a783e435325769ac01fee438a79e7edb1e521d908303043b3266e55a37c655d2`  
		Last Modified: Fri, 06 Sep 2024 20:58:05 GMT  
		Size: 7.0 MB (7024962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:577a5a18a6cd62a7d6babc803f5cd4f9dd75e10c22d67fd2055370edfa411b67`  
		Last Modified: Fri, 06 Sep 2024 20:58:05 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da1fc7486c748648addff8faec819d3b494b2cb8c7204e0e60f2dc112c322c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232760783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f89d30019258b1e4771dd0e8a6958b481c5a5ba43fe6cc19752e2b78b463673`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873cea8439d611411217ca493a0d1607057ba7484186976e82290b96bd05c5b`  
		Last Modified: Fri, 06 Sep 2024 20:59:01 GMT  
		Size: 102.7 MB (102729219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8574f3f6edd2fdd808ef43b817fa3244a91a1d2d196515810afc0344e7b0b3`  
		Last Modified: Fri, 06 Sep 2024 21:05:12 GMT  
		Size: 80.4 MB (80445295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18260b0ecd24707f233978b13fcc2c4bdc0726b4beadd58e84d0e55db9272503`  
		Last Modified: Fri, 06 Sep 2024 21:05:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f42286b84ee2019f2e5157be218ec968787e5690d81580d8aa9752e7425cf3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7045736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad18ec5e661b3d3da48695e913c92a4634c376c74e6e14eeecc73b485c77b`

```dockerfile
```

-	Layers:
	-	`sha256:06d2910c4f207d7b91afd4561bcb9d8b2b235d5f354b40bd374bd0ed79d42312`  
		Last Modified: Fri, 06 Sep 2024 21:05:10 GMT  
		Size: 7.0 MB (7031349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107556c87b9890a2c46c5ca5a7117eb94c86fe7d52368b939d6a0b6952168dc4`  
		Last Modified: Fri, 06 Sep 2024 21:05:10 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
