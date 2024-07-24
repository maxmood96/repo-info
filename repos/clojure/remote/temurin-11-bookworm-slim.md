## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:f0f0b1c3a79552149575329cebc814406d9d957e232ef27fb592b3211608b9a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a3cc6a0e53bfda2e7309bde799807039427c3cc1ea93c2eb5277b87aab971513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243744788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dced7021dd1578a54198bbca9fcbf5ff75ebfa1462256300f8be214f76279184`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931fadb73c06ce2d1faf10311bb134d55e9ad7d0b7c5350f0955532da9dc4dc2`  
		Last Modified: Wed, 24 Jul 2024 03:04:24 GMT  
		Size: 145.6 MB (145550342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10f66679b260b894c0d6f68d265d83e050a838f7cec55db7720bd0272d8893`  
		Last Modified: Wed, 24 Jul 2024 03:04:23 GMT  
		Size: 69.1 MB (69067512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169bed1585621ea0e6b73bc7e4f6535cf2df8e829abf78e10cd4258ff8cf21e5`  
		Last Modified: Wed, 24 Jul 2024 03:04:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43aca3be50b2cf95fa60b0006969bd654540d99aaf5e7ade61c30f78cbdd15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609ded64ba29fc49d8239808d0dab0ae513abf1a5c11eaad7ddab636352f8c6b`

```dockerfile
```

-	Layers:
	-	`sha256:2c88685a031a5c4ce2e5f9209ffe95e81b2b3537e4bb71f7631fc2ca52b0f36a`  
		Last Modified: Wed, 24 Jul 2024 03:04:22 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c5ea12fbe0da6801aa3af88fe19d4dca7089e3f9bba2b449c5ec815a00725f`  
		Last Modified: Wed, 24 Jul 2024 03:04:22 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e04d29e1f84952c09fe65b95f1e77835ea2bbcdb7558bfc3d14448dd232fe80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240279372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec35f3d4893a3fc4190938fadcf7ef2d507f2114110e928d024b2c9e25b39fa1`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55471a3be484fe97f862682ee638f4d91a474d190dd9e4273132f2eaab7d2ce`  
		Last Modified: Tue, 23 Jul 2024 12:17:01 GMT  
		Size: 142.3 MB (142304140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260e906da4db50710733b9af4bd3e6b4e195e06bce7d29f1993713de2b7966e4`  
		Last Modified: Tue, 23 Jul 2024 12:22:01 GMT  
		Size: 68.8 MB (68818017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f351197b9c702ea68129e4dec00591b327b4b3c74d14edf0e61f8a44bb3492f`  
		Last Modified: Tue, 23 Jul 2024 12:21:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:687dba435c412792b381ee7c6f61e0f0c1b6685c9a0b8ca8cc4bbbfd4469d462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cbdfce6396bd508791870d215c302a9216dd710d35b0e976e0059d194d8e2`

```dockerfile
```

-	Layers:
	-	`sha256:88d61971021745c6c04e1d37a501223038b12b6d08d8cda243b2fa9b9ba86453`  
		Last Modified: Tue, 23 Jul 2024 12:21:59 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f839bbd38b27f3d82edbfd1c4c6d349047b985e83fc0b8cb7f30da0144ab498b`  
		Last Modified: Tue, 23 Jul 2024 12:21:58 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
