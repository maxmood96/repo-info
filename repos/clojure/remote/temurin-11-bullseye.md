## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:72ef6015d4163b4a0237130bde1d412e9ff41d69aa6af92d0b62cbe96f0a6e27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9f5f2fbbcd3d0289f927bd4127c359c577d3087ee17b12bae07452e957157f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268500917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d278508445991c1998896f9952b243ad1903f20d70cd8dd1eab63d48ecde0b`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bc7e2a73a9912a1b4a3fb43d5f2958398d1c5b09c59456af83d777680c7c6d`  
		Last Modified: Tue, 24 Dec 2024 22:37:51 GMT  
		Size: 145.6 MB (145601503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbf86b82f3ed5df2b5b65b6b59f4601cda8f594e19d2f83cf51260aec650065`  
		Last Modified: Tue, 24 Dec 2024 22:37:50 GMT  
		Size: 69.2 MB (69159814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d1ffa70185c368dfe5b1ccf1cf7b327ec0d3b102d6115a79b3b8cc8f40cd2d`  
		Last Modified: Tue, 24 Dec 2024 22:37:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ca3f5540e017a747e8a6d9aa5db3a48dc60e3128f7c52ef7b1d2b80cd68aa8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355859d6851cf1b827aaa8a66df3c6bafe226a97f4a7ef036d9e1309bae87920`

```dockerfile
```

-	Layers:
	-	`sha256:cfc5845def32a54ab9accc7ae2a06ad6d92ed7b0ca259bc4f607bd41b66610ef`  
		Last Modified: Tue, 24 Dec 2024 22:37:50 GMT  
		Size: 7.2 MB (7224634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7f72a02a67c46db909c301ef68ff1d18171c1d43b474b98258ae31919afc5bd`  
		Last Modified: Tue, 24 Dec 2024 22:37:50 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80b2c05d5e0470d147082502ce617f4e901aeed3f8557a7502eb0eeceed51adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263921431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c18b44ac00f0b7a4fded3a666d4c1b94d6d977f2e8d59dc0cfe716a1f43cc6f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31265dc2fc7dc1111d34cf9c11ef92c4e266885ff7cc8263fe0ec79113f2c2ef`  
		Last Modified: Tue, 03 Dec 2024 15:11:15 GMT  
		Size: 142.4 MB (142389034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e0ebc7bd93e2b475d4b87ff80851f62c7a3a7464afa6bc5ac60ec003f7aeb2`  
		Last Modified: Tue, 03 Dec 2024 15:15:04 GMT  
		Size: 69.3 MB (69285759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f011de22621999d5b3f1dfcc61227d245ef68fa57ea7819a85fc848a59ff1ff`  
		Last Modified: Tue, 03 Dec 2024 15:15:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f18b539654365661a56e627376fa280b30a53807e73bf3ab11be3a33f7d95876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7254330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bcd3e4af4ba1ab88719d2074321fa9025308f8d02716b802005bfd48855059`

```dockerfile
```

-	Layers:
	-	`sha256:99d4430aac4fbaf63f3d7e20d254130ab7c23b5f57a1cb2ac3994b3852018aa9`  
		Last Modified: Tue, 03 Dec 2024 15:15:03 GMT  
		Size: 7.2 MB (7239960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9b7dfdcb85ab2387fdeca7caa8d28b365bf1476cce479ce89cca77019cff9cf`  
		Last Modified: Tue, 03 Dec 2024 15:15:02 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
