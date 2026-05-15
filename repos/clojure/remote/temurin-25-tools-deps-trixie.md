## `clojure:temurin-25-tools-deps-trixie`

```console
$ docker pull clojure@sha256:ac3ba61f233473319c3ff43579a8d1b8104ca11521e37faa56c2cd0e81520014
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

### `clojure:temurin-25-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3614e8f47c63d59c3fecd592afea997d5aaad98ac59c3aa2eca35b9b7e1c87d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227481688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c16d0d967737a955f73c8edfe4056521a469be832ff2b26f19e8009148f5af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:36:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:34 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:34 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f4164586195c49c89e37514e0e8e7556c637279e44f7442a464a8d17a47fd`  
		Last Modified: Thu, 14 May 2026 23:37:12 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bf97844978cce056f2317d1d5df842bc43807ea3f0873f547e27fdd9914eba`  
		Last Modified: Thu, 14 May 2026 23:37:12 GMT  
		Size: 85.6 MB (85603738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af895f70d18f8f13497e7e84badaa2b9d125e37dd7752d4b70eff0ba7d041794`  
		Last Modified: Thu, 14 May 2026 23:37:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f7f09d19e82cf91dddea1fc61ed775577327a552b63c950bb3e7eb36d9f12`  
		Last Modified: Thu, 14 May 2026 23:37:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:aff43d7905c17b593337440b7d6ef22fb1151735ddc78d29d4c8fb9cddf3e947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9fbc549c40827a61c3dc280b452b4cb82821dca1d68a12ff000c83d221c144`

```dockerfile
```

-	Layers:
	-	`sha256:73786b5cf8413d80ffbd2b77fea1711001075118d4075be300e3f8cb08159702`  
		Last Modified: Thu, 14 May 2026 23:37:09 GMT  
		Size: 7.4 MB (7439444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1515893420add4f7f5e1b7c84940c552c2d7d75640d8ffd0b821973505f942`  
		Last Modified: Thu, 14 May 2026 23:37:08 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f31b3b2436310f0ccab67d872076967d92d911382e6c5854a70cdfc3922dafe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226627749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f298a88f06c4568825838fba189d697fa1a47aad31e5b55dbe7a973e8747550b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:36:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:41 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:41 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4c859562b78362ea2f345a9e2eb4bcb945f3ffcdb28b9d1fa36d6ef4bd2ae`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1893b27e414727716d8804794e87e23ba93eb1aa7ad2bfe00c1bb3341c74e227`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 85.4 MB (85414999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1538780052c0b5984a4f189d64e3d6f86bbaac5896109a46d862e30c33a544`  
		Last Modified: Thu, 14 May 2026 23:37:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf5efd315af68ed8128c1e1d6d057278dae9f876c7cc4e84a85fdfb076fc18`  
		Last Modified: Thu, 14 May 2026 23:37:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1b4f73a0b199075d1cad013d32dbd0cae8fde353c518bdaa86e05580781dffaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a86ce267671317b69ba54713e8e702fac8687564900b35e7977c8ba43bc8c1a`

```dockerfile
```

-	Layers:
	-	`sha256:ad56cb711f7b9c412c715bdf1a162aed4f5bfad3373845cc6a97cb3ce2074d3a`  
		Last Modified: Thu, 14 May 2026 23:37:19 GMT  
		Size: 7.4 MB (7446495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bedeffef0682451a7b25353ac11a4a537896712657353a67084b521cecc015b`  
		Last Modified: Thu, 14 May 2026 23:37:18 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; ppc64le

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

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-trixie` - linux; s390x

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

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

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
