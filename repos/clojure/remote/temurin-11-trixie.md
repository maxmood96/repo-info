## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:72431c2e6314f299714fb3ceb00c38fdd39e94bd769c24a28d9235385f3c3e65
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b33de34d9cbb064d56ec2b1dbadadf1abf7e0e40098ae0640076950ab005f311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280759701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603ef863a78af9118ef014dc142cf91c9b23ed9f845cc87aef434f9ece9cd3b5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:06:53 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:07:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:07:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478feee6eb402957ee63eb6ffa7cf04544d6c231b6cbf1b444ea652528728a0`  
		Last Modified: Fri, 08 May 2026 00:07:33 GMT  
		Size: 145.9 MB (145886194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c391a5b3df278d4d23c618993849e2dcd20ac7ba721dc9133d24fa198870a7`  
		Last Modified: Fri, 08 May 2026 00:07:31 GMT  
		Size: 85.6 MB (85570760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e5387faf0f2b6c6a6f05fb77e99fde09b37fa389ffe0bd239b188f96463e99`  
		Last Modified: Fri, 08 May 2026 00:07:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a392146970019f0b247d299c5b033fd8d8f988f6578814a20a40a4ee0143dbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37fc6f20c9f49dec9ab3d7001e153d1d1ccd16d4d18b81ebb8612cf86e7d744`

```dockerfile
```

-	Layers:
	-	`sha256:b0324f5236cbc0e0bb1d3dbea6a89abece2917d07360e03b5ec34408ef512094`  
		Last Modified: Fri, 08 May 2026 00:07:28 GMT  
		Size: 7.5 MB (7490864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e57b01dc6596fd53d36cd6064d85832e3eb76b52c64219fa9f9f43497048e8`  
		Last Modified: Fri, 08 May 2026 00:07:27 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bcfa993554ed62b9d98b10d510114c75c276841c39b5d20e4f213b713a37953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277635474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdd84b57eff4cee3081c56529631ae92732e9057b1dd82cee10e15f2349ba0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:08:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:30 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b2b472999165028200a3763e277d5915819d29f4cc156a7db994c22c536d04`  
		Last Modified: Fri, 08 May 2026 00:09:06 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f248fc14bed724ee6cbead6f052812b6c127d3ae8cf3faec50dd7bbeb9c48066`  
		Last Modified: Fri, 08 May 2026 00:09:09 GMT  
		Size: 85.4 MB (85383349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4450cb9eb1aa0fe860c3dbfa788d9ba7cb6ad005f31d965ab24c6be6d3acefef`  
		Last Modified: Fri, 08 May 2026 00:09:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:efcdd2b93947220be96f565d2f27ecfbdc3aaa179e1a05ad533c8193659c1188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3194d4d794cbbcc9136113987fcc01db045f5663dce389d282445e17b2d87575`

```dockerfile
```

-	Layers:
	-	`sha256:c725086a451ae71f104b37420c1fe2c977e5adbfd171c0296d0f023f56c6f113`  
		Last Modified: Fri, 08 May 2026 00:09:06 GMT  
		Size: 7.5 MB (7498512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c2fd8313750c237952af251d4b3ac731e4cba81cb10e697fe86770f7569e8b`  
		Last Modified: Fri, 08 May 2026 00:09:05 GMT  
		Size: 14.5 KB (14456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f6ca2ba073636793e137f41c92494f106de01e45cb62925bd2f35c59660b56af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277220342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca5687d9b2159eacce17736a9e33591708eaa083581dcfc0a581f3ab6747656`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:38:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:38:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:59:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:59:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:59:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd298a1e1654753929706776995581c6d8e0ae8db97ccd3dd0cbc779069c0bd6`  
		Last Modified: Fri, 08 May 2026 00:40:09 GMT  
		Size: 133.1 MB (133110194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def5dc4b3e193610ce17e6036a10ce8955666adebb02404283755d1897ec84f2`  
		Last Modified: Fri, 08 May 2026 01:00:23 GMT  
		Size: 91.0 MB (90986520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46fd9ef36e4ff3f64d0e9ef2c9849a89932159242e3414ef6cb38b577853aa0`  
		Last Modified: Fri, 08 May 2026 01:00:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6c8b2c69c151ce0ea1ad7a1bf47ee89941378ba4342290482aacb86a4c8b8bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe51510bb13463e0b343dd59ea6de4e95fb28228d14e07cfce4eb7c95effdb4`

```dockerfile
```

-	Layers:
	-	`sha256:fc9c482f81631a4abc3df20e1e933300a4f1b78a725906e69b53302e2c54e715`  
		Last Modified: Fri, 08 May 2026 01:00:20 GMT  
		Size: 7.5 MB (7494670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b900915832fa19bdbc5b96220b4405ae3aeaa7b417923449d40c79ddafdb9f95`  
		Last Modified: Fri, 08 May 2026 01:00:19 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:86612c51c98329904fbef176f2c9e44cc614a4c9a28c9b8cbf6f4a84f09d6882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262570511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db681be2ebd1bfa30b89e86a98385a1d1cba06f12c46dcfe83ac8fc7f2b3c036`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:13:53 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3e96a498eedeba06f7eeeef03757ec4a5de489cdb2735c62011540f27ec753`  
		Last Modified: Wed, 29 Apr 2026 23:14:39 GMT  
		Size: 126.7 MB (126652714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b51d6ae365e0a5c9301fc1af27f6bea5a82ee27d4d256a49b1e9ef6985daed`  
		Last Modified: Wed, 29 Apr 2026 23:16:07 GMT  
		Size: 86.5 MB (86545048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a977154dba30fd808d8f4e3bb04cbd4d40dd1e3be6c9f63cbc3a59cd6ea8766`  
		Last Modified: Wed, 29 Apr 2026 23:16:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1279426cc1bd9eb33cf7175ffe948020cc0d12457c57af8627c916fb61ebbb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe6efd1e1b3c623d6767d16e57fa562efbd6cb9398ed25bf225161c508bcdae`

```dockerfile
```

-	Layers:
	-	`sha256:95035b2d9535fb282de7191ff7475729895a260fbc290c67ac314f92cad9ec5d`  
		Last Modified: Wed, 29 Apr 2026 23:16:06 GMT  
		Size: 7.5 MB (7486790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226aba9181fcd37b444a918060fb5a6ad6cad7570372089d4acfa768093ac00c`  
		Last Modified: Wed, 29 Apr 2026 23:16:06 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
