## `clojure:temurin-11-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:a029dbe59c69a07608a0c09d04644c30775538dc4fdb772bd312300fa76e1415
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:52361c3b5cab9194f75427c016d89fe67cb98424e883d97f8173d0590a32d9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262569997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d800640ba104284200d93a5ad02234b36da9d217a5ef3b90580670558f1c3031`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:26:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f484f4899b916ed417c82c7aa37bb645e2fe99792d260acb9be2a49341b94ddc`  
		Last Modified: Fri, 08 May 2026 00:27:34 GMT  
		Size: 126.7 MB (126651738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796bec288349432e6b2108364644f30c46e1e95dd569c93ad24fa983739f2a69`  
		Last Modified: Fri, 08 May 2026 00:28:45 GMT  
		Size: 86.5 MB (86545511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b882d4de74923ebc719a50b6e41e913340b21bb7d788e375d01cbca9c7ac77c`  
		Last Modified: Fri, 08 May 2026 00:28:44 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2aded721b98462f9f24c4a8e25fadf38548d53a9939f2cf6aa5eaa13475f08e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae418ed0127133df5ed92458f93622d20377bb9d2ca1399ca4fe229ab05f6b3`

```dockerfile
```

-	Layers:
	-	`sha256:0c084416b9a73a76d2509be6e1ddd0f18a6b74f0c4b6a8d3aa25d6fa89c1f90d`  
		Last Modified: Fri, 08 May 2026 00:28:44 GMT  
		Size: 7.5 MB (7486790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9adb4f9c010ef025f5e6a5710e170e147712ced6d3186db727031e1610b2ef8f`  
		Last Modified: Fri, 08 May 2026 00:28:44 GMT  
		Size: 13.4 KB (13384 bytes)  
		MIME: application/vnd.in-toto+json
