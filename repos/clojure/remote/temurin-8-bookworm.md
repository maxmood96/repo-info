## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:61dac4ecb0826c7d61f06c4c31b71b6d8b4b46e75559c756425a70c83bed5733
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a47a562e8edc1ab0078fa20e7643385d444a4392293adc3655b3b4d16ffb0523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233666007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c10a1f900fda402af992cbf2092282bef85ca76d94f809a31a4618d46153bac`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451088f992cf0b3174a2eb3169371425f202b5ce2a4d9819e81b4970c7bb2230`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 103.6 MB (103600203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d6f8317a438d6910941853569ed88a8a716ab53989de89173dc0e6ec36208`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 80.5 MB (80511095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5bd71ccc81673910c72900a1f914c428ab4f5e1fa0ceaee79c154c99b977de`  
		Last Modified: Tue, 02 Jul 2024 03:02:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:72365d320e7ceb6162513c7a5e0d5eff3d62352a05b99a21a3c5d6da6ef8de1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607921a732a3957b863bf973d2a7ae9591dd4deb94377e5107517b0ea746111e`

```dockerfile
```

-	Layers:
	-	`sha256:3d8e5fbf4b04513f10d0de247c41aabce3cbc7190ea06bd2b1337b8c76624a40`  
		Last Modified: Tue, 02 Jul 2024 03:02:45 GMT  
		Size: 7.0 MB (6982449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e56448b9d4d2b5f6c2ac41adf3d0b03d4b735f9fd36ca7461773a6af5629bcc`  
		Last Modified: Tue, 02 Jul 2024 03:02:45 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80673afb6f294dae96c2bbb8591d48f57697c7e6a6d84859cab10a619469e5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232359282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca9a0d975f0f7d00833403cf38d2817c2cdca0ce66baaaa287bf8c228eb1069`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
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
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6e9ecbdc3ddf118977ce6146d477e95e017b027a376970e58b440ff008a5b9`  
		Last Modified: Thu, 13 Jun 2024 11:09:40 GMT  
		Size: 102.7 MB (102700388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d57c15b94be762ea9595f29ef21f8e920090b15b7c45195d49e434bd400f06c`  
		Last Modified: Thu, 13 Jun 2024 11:23:59 GMT  
		Size: 80.0 MB (80044843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c136e552c3c401165b050089010f937b995a05368d5ef1a03cb827f2b358ec0a`  
		Last Modified: Thu, 13 Jun 2024 11:23:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37c8b9c93257debfb3f0816bd1956671b50f2a9c4ccff1224a0884963cd19802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729c576e6018b3de1894c6df8280c38bc99df32b36e3b9432fd6b6e23c6c392f`

```dockerfile
```

-	Layers:
	-	`sha256:620e5b8f911c7df9b9bde6dca6eba5f9d4e486f2bd50b64ce02d012a2717dbcb`  
		Last Modified: Thu, 13 Jun 2024 11:23:58 GMT  
		Size: 7.0 MB (6989541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a47a9042c1cf709e6b9acceeebd31c42ca51a769f339d57412f7eb66c9719c4`  
		Last Modified: Thu, 13 Jun 2024 11:23:57 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
