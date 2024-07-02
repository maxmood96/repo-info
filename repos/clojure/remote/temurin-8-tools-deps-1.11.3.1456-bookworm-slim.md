## `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:b81e868fed073fb086f940746792ebb8af36036a6dba614f6bbdc577960b95e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff74e953f5e61773d7dedca4fef7291686db7ddb79de2675e748c94ecc2384d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201793709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05809e9cd4a4cc1208882db2a66660482494ef8c8dba5e7a7bf1726a7bbe2fc0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e615f1a766f666964c1b5ea5fb1d95923266c8490aa42984c363650243892e`  
		Last Modified: Tue, 02 Jul 2024 03:02:45 GMT  
		Size: 103.6 MB (103600211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eb24804ba653d4213eb15fb2566e055a1fe77a510d46c78ff072d49d7ba647`  
		Last Modified: Tue, 02 Jul 2024 03:02:44 GMT  
		Size: 69.1 MB (69066575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c58a447edfb9a52fa33c63d897b481fc3dbcdbf6181867da94a1c2c5b874265`  
		Last Modified: Tue, 02 Jul 2024 03:02:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf2de0ce1b84ccd0a9ed7ee7faf0a1eb855dc60e11fc55a0579973a9535723ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4741447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6abadd3dbdf1d981118dace2621bcb740caaf8854af73d064adf3943eb4680`

```dockerfile
```

-	Layers:
	-	`sha256:724073562f834eafcbbf07a4d1bd948b1c7bf8475910a3a2c9bab58ca784bd5a`  
		Last Modified: Tue, 02 Jul 2024 03:02:43 GMT  
		Size: 4.7 MB (4727527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d1327bb4d9b20b32d7cc599611cc81d789972585f42d03985bb04a7681c2b3`  
		Last Modified: Tue, 02 Jul 2024 03:02:43 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d3f3b0e42f044fa2d05df85fcd8cb494d6beef6b5d3da72d2401eee9704f08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200501208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507a3233f6477684d7df13264a9313b45461f623b54712cbe53e26110a65365a`
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
	-	`sha256:4ab2e61ffd9a81e8a8962bd8afec8741dfdf92978bd880ae8228d1fb558eca13`  
		Last Modified: Thu, 13 Jun 2024 11:21:17 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2605297d0c66832f95c152dacedef5f44e01743fe01f126c6f95e516384fd2d6`  
		Last Modified: Thu, 13 Jun 2024 11:25:47 GMT  
		Size: 68.6 MB (68620493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7492410e516c81137a2ef783385c26bf87d8dcbc327dcfd40539839eb8aa31f3`  
		Last Modified: Thu, 13 Jun 2024 11:25:44 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb7fe2302bb08654b7730d53cde283be376ee75b32b0613bd87c47fb0491b6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4748271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f843da8a682b3d0498a3b436871982f67b47528cc130d9c8479c649003156470`

```dockerfile
```

-	Layers:
	-	`sha256:c809a5a1d29cfb967a92b0b54af3d76ac8bcd0291d445f6cdc8a5cd16f3baf4e`  
		Last Modified: Thu, 13 Jun 2024 11:25:45 GMT  
		Size: 4.7 MB (4733811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b861b9e5181cf0bec969117193b45401b12398823a3b0a65bcd58dc296e94af8`  
		Last Modified: Thu, 13 Jun 2024 11:25:44 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
