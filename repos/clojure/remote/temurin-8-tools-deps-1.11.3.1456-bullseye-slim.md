## `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:45d2355ffd9f357b29928feb04f32812df95278df95909139eb829885df78151
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b2be7257a33e929775d1d061253a09a4335ba536e2f4d63832e4d6b6df7f6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193454417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a55fd2e0a651225cba2d468ead1aece892bac9355e9476cb61f87eceaddabf1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e12b95760a35d4c76eb751b062abf0b3ccbf8b606b9738ddb8a69aac67628e`  
		Last Modified: Wed, 05 Jun 2024 06:10:07 GMT  
		Size: 103.6 MB (103600201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6309a6be53354ca4b8eb42a27e631016d7254cd6f3d632be508409e65ec2bd77`  
		Last Modified: Wed, 05 Jun 2024 06:10:07 GMT  
		Size: 58.4 MB (58419636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b2aed85635ec0caeb291b113a0ef7d123faaa15ff57fd04e9f4566225b818`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c8c1c2053c3c755774a570002ee069c9fab439ed7b8e263c1f18db41fd5e850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5746e5dbcebfc0bb6b4edaccd054e53d2792cd9e40559aac67725ddd4dd8ec18`

```dockerfile
```

-	Layers:
	-	`sha256:765c51b7556e9c9c49855a9cf3faa1c92de9aa14df2ab4d2c0069e148d583791`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 4.9 MB (4931721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4c2d444c2326198af864d044dd619f1165ba2e65faf7e61b169d1143c4245b`  
		Last Modified: Wed, 05 Jun 2024 06:10:06 GMT  
		Size: 13.9 KB (13870 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e692ce81e7ce30ab2adcf8aabee5a2f281dd778d31e8bc60c25e34cce775652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191327992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a676a80acd8ba3f6cdfcfacb05752f2f985109ce36ebba21d96ce2b9c9356c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96413e5e1bc47e07d164012b8a21fa2146eaf62aa0cf9162f8bba4071fc67e6`  
		Last Modified: Wed, 29 May 2024 20:27:29 GMT  
		Size: 102.7 MB (102700442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03650e60b74374ed855ac4bbb8e075d1db7d66e70ae253da95861bb4c666633c`  
		Last Modified: Wed, 29 May 2024 20:33:02 GMT  
		Size: 58.5 MB (58539995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147bc84ea4010db4672b660c609189389e0867f3fc1be32e84dd36532881e2b1`  
		Last Modified: Wed, 29 May 2024 20:33:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90227eee050729d4c5040de1be14d59c53515bcb811214835d5c18f7cd2261f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4952489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a4fc449106e0898252e25e5cb8f0a23a040c03dcca68ef2a5ddb66fb220626`

```dockerfile
```

-	Layers:
	-	`sha256:2fa98f671b5a1717db56a9bbcb7adc9bb2cfe50fef19295ba265c83e54f11867`  
		Last Modified: Wed, 29 May 2024 20:33:00 GMT  
		Size: 4.9 MB (4938078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54577a8dc3f9add66533bffe62db59b3c06f418a83006a728a110589eb548683`  
		Last Modified: Wed, 29 May 2024 20:33:00 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json
