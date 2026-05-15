## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:c7f13e3ae2e04bb01d2dd6c864f48d101a7e5b54502d059086f27451f529b121
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

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fcdc53557b9c221fa8c75c789e8b7c7d96a322efa0cdbca8b1fd28271357e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227481488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34913f2d5a9e244459b8731bc8b68fd7de1e8cb479309d64aee2eb43ecadd19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:10 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012b166ac5adafce01ad3e58a07b9d3c7fe050f19bd742b5c9e2299c775bc0ac`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385801ca07d21c19cb2c6e80fae8b86e47aef62926733a99a77e4fee511b3511`  
		Last Modified: Fri, 15 May 2026 20:16:52 GMT  
		Size: 85.6 MB (85603537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39802efcd3c5c47d45ac0891763d03e5193246fa35c94baeee014a19d1fc249`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b09360e82c7bd08e3d823e26e4413a296e5d97a41ceba53c8925265f17b87b`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4975f87102740f5cc943c4cd6c6581098df7f99a2481805e9542f335788228ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d755d6d5555478cc76157ce8b780ef94c5bb2cc4dfd8241318180ec2b0d1a49`

```dockerfile
```

-	Layers:
	-	`sha256:9a16e0fd8d2bc2d9458c6a2fad397df1782376c43cc6e164042b51768eba0f9d`  
		Last Modified: Fri, 15 May 2026 20:16:45 GMT  
		Size: 7.4 MB (7439444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806d56aa3fcd04e6675ee15e1cb6616811889650ecd2b409a0397e508fc9bdcd`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccd4d8e29d01acd13c9a9a9cf7be7c3c77ca2898380660705f4d0cb0b38083f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226628154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de11384bf173ef60dd838e3f15559b46b8718b1031d1552ffe89b716e56015d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:13 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a585bc135b4a7328b968a7e3ea6be7e3de0a30a835beb50e7136cf297de6c3`  
		Last Modified: Fri, 15 May 2026 20:16:55 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20b1ad8544deccfd1f8733615fb5c357c6823df48ffc40d4376e989a6fc4a6`  
		Last Modified: Fri, 15 May 2026 20:16:55 GMT  
		Size: 85.4 MB (85415413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442bcfc4e41d9c84dc6aced5ee267ec87725aafcb24a6408ff0da6ae2e309932`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859fa332166d6ed8f8fb37c654557551904985c8f1db4b208f5b4bea38539817`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:607766a76f55611355285b4372dd8cefb2285b8b550790e1f985117312266924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeae80a4c1b72e73387cfc2f0ca726bf15c62de5c85ea32b08df4a82d19c764`

```dockerfile
```

-	Layers:
	-	`sha256:d27d6f7b7dd1bad2a8ac96227fff63fffcd47ddc993cc153e93632a04b0efb75`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 7.4 MB (7446495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8773b35ad58d1bc82c7b3b3f1e9a1689aa1b9c1c5c4c08f590c2bf89eb2b197d`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:77cde2ac4a6a86c5941487876f4043ddb86b8c1ecd219775e68b6fe7e5592d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236046652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32500b4e5a99f9b6e0a103c13250d1a3deca58a92e34430a466fbcb9dd176627`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:42:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:40 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:42:40 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:54:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:54:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:54:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:54:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:54:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2325345b811e94f6ff3ccd6a646a97c3cc4365dd97daee1fdfcb79b03cec8cfc`  
		Last Modified: Sat, 09 May 2026 02:43:51 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86508b343dc77d764a173cb94ba5108ef741dc04b0f5939038db96b2944d7391`  
		Last Modified: Thu, 14 May 2026 23:55:21 GMT  
		Size: 91.0 MB (91008414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442339c597e462c8d3c7dd219f6d124eb7da3e49d9d6061319d9a5e7d9313ec2`  
		Last Modified: Thu, 14 May 2026 23:55:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014e76ce95c223c86751dc87e723fcda41ed9d6d94931f29ed14f0960cf7122`  
		Last Modified: Thu, 14 May 2026 23:55:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d7a98f603ca5ec8416c25434104574f247a954f457594617830d41d4d2e57fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd61546a6906374fb29af0b9a24834062a7217b1f0ce2e2cac3cb380738820e5`

```dockerfile
```

-	Layers:
	-	`sha256:7bcc5bcb5e14e246b2a036aa78dadd787ef166a3b9dc057a5eb4869b65292de6`  
		Last Modified: Thu, 14 May 2026 23:55:19 GMT  
		Size: 7.4 MB (7427189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32b2365a16c5f51cbf1e2b713a88600822cdaada3eda3544f7a50886eeaea3e`  
		Last Modified: Thu, 14 May 2026 23:55:18 GMT  
		Size: 15.7 KB (15676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b06ec6630e52169d86f36e7492e98014eb78a823c5d64dbd6fe6bb03e50cdd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224359844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd852e475bf7b773398dc3d94ee57fce9ffd058413da40a0be40e92cc8af213`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:37:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:55 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:55 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:38:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:38:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:38:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:38:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf2a6bcd4a7e1e95003b939da80bfb605c51a2feb83067b2ab08434c331cfce`  
		Last Modified: Thu, 14 May 2026 23:38:41 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad8a4990cbe0dc8425151b8818e227ad9f6062bf7c1084cb8e1e05b766bcad3`  
		Last Modified: Thu, 14 May 2026 23:38:41 GMT  
		Size: 86.6 MB (86566158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc5049d5a0afc81e4daa261d2fa0304be51e188197a0001b181fdce142ea3fa`  
		Last Modified: Thu, 14 May 2026 23:38:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b01178f9619070eaeaae48070c33a053b520aee23250e91c94bc6130794d91`  
		Last Modified: Thu, 14 May 2026 23:38:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a5af5c104729f06b32dadee5fcad47de89a981de13d0cc97a1d5e7ef2ac6f5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9697892074b1f2ef75ff1be897d7d35f96c68248cef0b516fdb3ce777cb99017`

```dockerfile
```

-	Layers:
	-	`sha256:093e1f486ab78f8f149b2cca87e481a580664c9c66cc91e065f03fede89d0093`  
		Last Modified: Thu, 14 May 2026 23:38:40 GMT  
		Size: 7.4 MB (7419928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3ebd5a4020e0a7b315275225ab311febf98278095a2a3b3941838aa8e21cc58`  
		Last Modified: Thu, 14 May 2026 23:38:39 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
