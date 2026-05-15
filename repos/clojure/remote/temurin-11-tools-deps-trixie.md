## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:f89755d0be222085ecdd836b6abf18299e40a28f40df32a5c9a5490a42436dd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6927f22f9f91fd6f901f5a96b8f77558e116ef71d2e30167d91836245b0d1e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280792952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cfb2e3ea18affb794153a9a33ce1688175a122fd0fd541263346f4786fd7f0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:15 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eec339cdcf93fdc7dde580c03faa8b7dff56608e859569a19762bf5dcfd25b8`  
		Last Modified: Fri, 15 May 2026 20:14:54 GMT  
		Size: 145.9 MB (145886218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53af09d51d7040a8e779df91df55043eee0d31b43400c9754f89feecd49624a6`  
		Last Modified: Fri, 15 May 2026 20:14:53 GMT  
		Size: 85.6 MB (85603766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fe54fe9b776a9f566e5d7bfb32ea22afac122c4d15d534ef426baf9cb39246`  
		Last Modified: Fri, 15 May 2026 20:14:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:317c0c1a804da37c81780fb8ec84daf416a72fd92802e87730079dd53fd84ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a075068c10b400dac7260a641f352807e512fde942584e69eae34fb060ef65f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d2e29387ddc39f0206911f3cbf803e4602263db476ae55b9f1f4c4f7d707d35`  
		Last Modified: Fri, 15 May 2026 20:14:49 GMT  
		Size: 7.5 MB (7490898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14319fdcd49cb5b3d7cf54bdf7e2c6d256381461fc840cd59eab9b2571dbf24d`  
		Last Modified: Fri, 15 May 2026 20:14:49 GMT  
		Size: 14.3 KB (14338 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:162a90017cff3204d17add5e7ad9e5714cdc32bc254f510c3b92bc83f693c515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277667297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981f44422bc9e6e09157197e441cb8f8594cf8328d2f22b7932568cf79f631f6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:12 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:12 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c320c6980c1a0f6ad63163269cae91fa206f794277cdff4986601f2069fe1`  
		Last Modified: Fri, 15 May 2026 20:14:53 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c3605f26072a0e76085734c012b6081d581c0e893e9318796f4753662b6b6d`  
		Last Modified: Fri, 15 May 2026 20:14:51 GMT  
		Size: 85.4 MB (85414974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4434d98f2cd651b97c58017d1c3f62b308bba4792c4cd21f06f0e60b841aa29`  
		Last Modified: Fri, 15 May 2026 20:14:48 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0d36e9864b17167a0929bbc11bfa9053e90a0941e4742019ad83df373c8e82fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505dd0919ad56d74a34fb7bf3b02ecc572bad813fcbd7ea91adf8e1bc9af8441`

```dockerfile
```

-	Layers:
	-	`sha256:c738dc6dffdfe52744e40820ac70725490612ebb2717cafd2bad34da05d816c7`  
		Last Modified: Fri, 15 May 2026 20:14:48 GMT  
		Size: 7.5 MB (7498546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65500a15155ae713aa17f3668d7c6976bb6c4323c89ed83f5bff9926e057fef0`  
		Last Modified: Fri, 15 May 2026 20:14:48 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:05fabc46c897817ff30aff8e3a232ae83158b06edcd03b3b6cc0cef2eae10593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277240935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f47f7c5082ddb6263e5aa4cf3edafe2c535ddcd4c0badb9262c5ce886f13078`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:20 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:26:20 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:21:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:21:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:21:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6819a6f95dd2e4192ab6b7dae90a40976321dcde2fda4665eb71bbac73d5122`  
		Last Modified: Sat, 09 May 2026 02:27:27 GMT  
		Size: 133.1 MB (133110167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff49e822af717e234b91bbaed5ed00ee4f47ac07108b9190afd63c350d995ba`  
		Last Modified: Fri, 15 May 2026 20:21:41 GMT  
		Size: 91.0 MB (91006955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce615e65115be1342d8648c2db9beeaf4a12533b06b89e5f7b336a70a73bd2e`  
		Last Modified: Fri, 15 May 2026 20:21:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8862e75fd74c43724cfa30e7058c52e16bd0605a6e7689e60b9b1d420c62d4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516cec7e6287bf8624cfa8ad7a7fa51933b7f9d12e111a4e1fc9e2b254285beb`

```dockerfile
```

-	Layers:
	-	`sha256:d02bc1d7c0abeb09d62f436dea4c689d337d7b44911fc88529cd54e379cd68fe`  
		Last Modified: Fri, 15 May 2026 20:21:38 GMT  
		Size: 7.5 MB (7494704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2f0cdda3731d6f7c1b54e43189dbdfc07c28cf24a0d9e2d609de6ca994dac1`  
		Last Modified: Fri, 15 May 2026 20:21:38 GMT  
		Size: 13.4 KB (13432 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c68d7eea7c4068d0ce2b8236dcd7b1afdcff62f588dae9c75819a44e46898e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262591672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190725cdccd7f07c3e7727df38959e6884e86c7dca227f6efb9ed60896d7b13a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:45 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:46 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c8c6065ad7c76b091e258045d75213f8970d8f170ffa27f4de19b1ea27fcd3`  
		Last Modified: Fri, 15 May 2026 20:18:00 GMT  
		Size: 126.7 MB (126651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806b5bcdc73821d904db580ff8784fed05c8be4a5d48d3b5fac557ce5419ecb`  
		Last Modified: Fri, 15 May 2026 20:17:58 GMT  
		Size: 86.6 MB (86567004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd669a44e4030ec81df4ca1fe60a87f3d58e114872870b6243e717312cd94601`  
		Last Modified: Fri, 15 May 2026 20:17:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:46ea7e79fdbdbb9794484cec4b33350b020fe021d636a05d4af3f4869d0efacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3811aa3a20ba673c635b4dbf229315f59cb751cd9861b3f6e5b1c204fa9a560b`

```dockerfile
```

-	Layers:
	-	`sha256:f89e86bf944d4312844ede4bf35d26c93065bfbb4a58b2eef30b2ae8272dd4c9`  
		Last Modified: Fri, 15 May 2026 20:17:55 GMT  
		Size: 7.5 MB (7486824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11e00a87410cef9d0c98d5b6056767c9f53bf9513f51021dea7d9da9bb013e2`  
		Last Modified: Fri, 15 May 2026 20:17:54 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
