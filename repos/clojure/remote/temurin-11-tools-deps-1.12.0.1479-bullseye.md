## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:77528b311b8875ddff4a692585ede36dce940829ac857bc18ed0c27e3db18839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8fdead77ad731877043087279bfbd26d99114f276313f45fffc746398bd14746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268499732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9256955a87e24cf13974ac410031ead97c81dfd5a2167923d3a3adb38addc`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eee3a330b5e6e63668b310d9b391ea0ba561a34d233e492a71783d6649752e3`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 145.6 MB (145601429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103dcc0c9db920d2bd714da0275a18b5fe740068752517a632d5ddbf2e6bfc18`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 69.2 MB (69158511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b21a9284f170dc18e0d85af5b6fc4746a8d7a2cc2f6fdcdddd056cf0612571`  
		Last Modified: Tue, 03 Dec 2024 03:19:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b8ab42c8b8cf51f79b33132cd31936b437154c0a2f04e29d8e3d305e4a62f0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7248490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b841c4517569ddf7f944830051ef02a6f7faed1e72bd8ff05a0befd6e215eaf7`

```dockerfile
```

-	Layers:
	-	`sha256:04f42dd2f6400cc989b64d1059f763141432236fd64aa8d10f7c336e233171db`  
		Last Modified: Tue, 03 Dec 2024 03:19:30 GMT  
		Size: 7.2 MB (7234238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59b39b4244cc20e4b885a1e0db468e929773020f7f1bcd4e8a9d8ae1d22883e`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

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
