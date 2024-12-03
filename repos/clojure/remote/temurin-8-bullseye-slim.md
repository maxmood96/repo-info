## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:8ab90d5e9065709ffc92c3488586e21e24ee819babee8ba034788a7e0bede217
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e71012db1261e550e2111aa91f0d525b3cb4298c8110b5ba0575a4b521f28f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192643756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11541c0f74200b41f223f6a84616be1db1a394d250dba89152163fe90acd1ee8`
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c20aca2044aa1bff7aaa0118b927cb52cf7ed8ff5de202f84ac4cec3324b49a`  
		Last Modified: Tue, 03 Dec 2024 03:19:23 GMT  
		Size: 103.6 MB (103633965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be76f2a1e2548d20a21d624c8a3a0bdd7af6daa538fc297be8fbbb8c256312a`  
		Last Modified: Tue, 03 Dec 2024 03:19:22 GMT  
		Size: 58.8 MB (58756505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c6ff89fadea016620e3ca3c26faa2307fd4c3e3a244f1e0189d60fc502456d`  
		Last Modified: Tue, 03 Dec 2024 03:19:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30517cbd215c092eb4919c920c591b5bca68ff977a51efb94abc8677b2328229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb2bc6e9ee9f5adac00a5a7009651fd6a3bfd95b9a72ff268af8848cc76302e`

```dockerfile
```

-	Layers:
	-	`sha256:a9887e7a0997adaf7611df60ecbb9229d0d740ea152f57633087198160c8f894`  
		Last Modified: Tue, 03 Dec 2024 03:19:22 GMT  
		Size: 5.2 MB (5245719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:474718147b73e28469790f6093aa3a1bb5ec87d1ce09437eaad4a854c303155b`  
		Last Modified: Tue, 03 Dec 2024 03:19:22 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77bff8e8fc5ba93c512c046364eb3b465cf2d2f8fcbbb079c7e23aa642bf5fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190373616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2affe06c124a2ddcf308067d180a424c2544fce1440bd6ac719568404289fc72`
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5004855b7bb2c7db6bc64471c5e9b9b7737ee2673220c268b8f5feb653a54e00`  
		Last Modified: Tue, 03 Dec 2024 15:03:58 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd367d6c5041d4b5b22261131e963f2350fb7c3f4fe3924357e0a20a7165e71`  
		Last Modified: Tue, 03 Dec 2024 15:07:48 GMT  
		Size: 58.9 MB (58880332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58373b123069ca5baa343c208c393c7a7c3d966abccb259f564c94be90ac290`  
		Last Modified: Tue, 03 Dec 2024 15:07:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb19b0b236a99b7165c7a77fc48b0fa22059b48c1e960454de9e1d829b1bb0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728363da0852291aadf255575dfb333f1b1e1c538bcb1f16163498d7d3cd5bc`

```dockerfile
```

-	Layers:
	-	`sha256:4a979ab40e4563f5e465170b151aeda926346388647d51317b228e31939fa238`  
		Last Modified: Tue, 03 Dec 2024 15:07:47 GMT  
		Size: 5.3 MB (5252155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135b5392f0d759b7be0afb01671a6368436a2f3d23d46f012685a7dc8009073c`  
		Last Modified: Tue, 03 Dec 2024 15:07:46 GMT  
		Size: 14.4 KB (14413 bytes)  
		MIME: application/vnd.in-toto+json
