## `clojure:temurin-8-tools-deps-1.12.0.1530-trixie`

```console
$ docker pull clojure@sha256:f258a2833eb645ce7b333b35e1b2ec3315e5f4f332404a1139788e1f450d3fd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:5ce87592298205c13b05862bf821eff8bf506a5ab089f619968a85b07bb526ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192186527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa04b8229b7097e70c9a37349fe981f6b3aefce429bd2400a5daa86aba8aaffd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991ba0099e31d5876895014c5273307078ddd690c1f52f2f98d8b9b4dec0e74e`  
		Last Modified: Tue, 03 Jun 2025 05:15:32 GMT  
		Size: 54.7 MB (54716190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800ca6161cb73a5cff81ebab1234450a3d7b41340aadf88e80a736aa084706f`  
		Last Modified: Tue, 03 Jun 2025 05:15:35 GMT  
		Size: 88.2 MB (88222785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0200f6663565b580ac2a7f173d82323696aaed2c83153d11459d445122db63e`  
		Last Modified: Tue, 03 Jun 2025 05:15:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f9fc0158dbcba87d987ba09e8f837a21d67c764dd27b4b28c922e9d3fda70c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7454238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c04cf7d5e26c78fbb046c6f31b0264d916a0f9c54625ebd5cdb550452d3c73`

```dockerfile
```

-	Layers:
	-	`sha256:36d1c26e7bb69adf16677a6f5a13423928ec1d878bee7765cc1e246e83c08df6`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 7.4 MB (7440026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1099f2508c6fffa74f1817db0d86c54e1504a8f9ae7e86c53294c2b860567c3`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3460c1546ff1c9b6bf0efed47b56e7c34d6db5c88b1bff58f30235f570fcdd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188624569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae97fad50db0f4208e859f74e49ce5dfa7fd0b22d605587702ae8ec5af40715f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0750f2222ba634ef6acb4ec68d0f6477201e94dc5d4d40912170cc287948efb0`  
		Last Modified: Thu, 22 May 2025 08:03:30 GMT  
		Size: 53.8 MB (53830506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e08267b6e2f571740dff57c9357fdc2dde64bb7c7612735e00782380b0790b7`  
		Last Modified: Thu, 22 May 2025 08:07:54 GMT  
		Size: 85.2 MB (85175126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eec74de994295e49ce241896a50bcf94ab10f566a21075ad278e76512ca0577`  
		Last Modified: Thu, 22 May 2025 08:07:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:46ea415b9eb7d7a4bdd528eef3682b0dadd1fe505dc984cf26ef8d36bf5de19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380f488f19f919d50f81f66ee841594913222af0ced8db14c7512e0660ecc92e`

```dockerfile
```

-	Layers:
	-	`sha256:801afc6b636943bca6b6d941baa5068470c2764a2f5c02660c10dea9b33d8400`  
		Last Modified: Thu, 22 May 2025 08:07:52 GMT  
		Size: 7.4 MB (7447754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd4d09c5b7cacd52063c59bb161e0e2563e16811b9b894631af003a8b22cb90`  
		Last Modified: Thu, 22 May 2025 08:07:52 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:aeef8baaa2638312598bd80aaf0de7d3a80c90fc819e9dbf50b5e46d76842d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196000695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677aae489aa176a98b15e805ab9cb9cf4ef2aa47a75f84969d7d615ffa0a036a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a07b13006a8a0bb4612f6495964d16d8d8f3260cd6caf214f944021580050c`  
		Last Modified: Thu, 22 May 2025 10:44:42 GMT  
		Size: 52.2 MB (52167929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb112384de037c04eac558038ebfd497ccf253b8ec1142f4b996989a58867ecb`  
		Last Modified: Thu, 22 May 2025 10:54:24 GMT  
		Size: 90.8 MB (90751576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c958e9c5752f6bdedfbb6eecb24c0d6a2c46c22639f7c7ef5ffe8d9bd6c2dd38`  
		Last Modified: Thu, 22 May 2025 10:54:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3b8023a1978ef8860584b3130ed859aa36fa6faa95378444a8e10df2e21675e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad3fcf07f138b04f99a951dc96fee4691973f1c466ab5d5994047e09f1aa560`

```dockerfile
```

-	Layers:
	-	`sha256:6cb9e3016fcc4dac69bc6a8a1b84ef7980508358a05427ec7caf2e96fada03c7`  
		Last Modified: Thu, 22 May 2025 10:54:22 GMT  
		Size: 7.4 MB (7445036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8debfbc34a54f0fcdc35cef322020c0e79e2702ff2250e03effa55a0727eb1`  
		Last Modified: Thu, 22 May 2025 10:54:21 GMT  
		Size: 14.3 KB (14260 bytes)  
		MIME: application/vnd.in-toto+json
