## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:e73f64a166565e22d775b287daf85ae3ac5b1047c0f1ca15894d8e807fd95aa5
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
$ docker pull clojure@sha256:348bfb0a7ff68b6dac7bdc22a7c1dad83afbe74250324b270f4461d6137ed9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191716076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae509aeb0c290246d71bc6a98874874adf89988e9804bb2adbd94d04fb8e7095`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90545bb27805e104123f01b3e16835ce4f6e45b25a39ba2f670aad5c259ca992`  
		Last Modified: Sat, 16 Nov 2024 05:14:02 GMT  
		Size: 102.7 MB (102747710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f2f108b24a554ddc836ebfd65f70a3e9943c041f64d50d671409d48d5b99d`  
		Last Modified: Sat, 16 Nov 2024 05:18:14 GMT  
		Size: 58.9 MB (58876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67b6507464b438a14f5097f7225cd37a11d047a6f0c1c193bb2b57203ca3422`  
		Last Modified: Sat, 16 Nov 2024 05:18:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:37a19328b9fc1444623ba3571f53e2125db9c8b78b585ae23042862771bad68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2c1fbb9694ab664016402ea708d3ce79e46902cb321d0ed9228ad44e52c97c`

```dockerfile
```

-	Layers:
	-	`sha256:e3160d75d6407930453a806451bb503dbf58ef14b881882ecedac2242cf2467f`  
		Last Modified: Sat, 16 Nov 2024 05:18:12 GMT  
		Size: 5.3 MB (5253958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd47001902560f19bd37dd3a186eceb03b53d2a6b67b92fc245d7e083136a51`  
		Last Modified: Sat, 16 Nov 2024 05:18:12 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
