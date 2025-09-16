## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:5d8a85fcd3760923dbbf870d4535b110564ec49fbf8e5e9580c87ed5812223af
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
$ docker pull clojure@sha256:e5bd3dcfa24d6dc04a0b7a4f98958e69ff45c2e11f9e2976445d6bcb18738b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280471779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd483dc34444ea2dc36a327a57041d8eb775aef15177a85cc4d06457c1978ca0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325f530dc6cf7a6ed5d3861baa6dc807c5e83eea82c2fb0326328f25c2f48819`  
		Last Modified: Mon, 15 Sep 2025 23:25:44 GMT  
		Size: 145.7 MB (145658233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a696ca196e6af4186e3470cc2cb53646173ddb41386a70303c1b98a9df476f8a`  
		Last Modified: Mon, 15 Sep 2025 23:26:12 GMT  
		Size: 85.5 MB (85533373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700269ebec84d2c67c83306ec15b1faef4e064ceab1f2639ca90b5f93701bbd7`  
		Last Modified: Mon, 15 Sep 2025 23:26:02 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:62493cc1638dde0010981e09f3bd91a5d590351b21202728698cfcbe3ffea0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653879f43cd92c7f27a081c389b32a2731689151e0a6e0a0e55d36e16e819061`

```dockerfile
```

-	Layers:
	-	`sha256:5c6ab7f2e3834bf6d1ad37b8ec26872775037f651edefb61d4772ad84ed34f57`  
		Last Modified: Tue, 16 Sep 2025 00:37:55 GMT  
		Size: 7.5 MB (7486986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38505331636fa6d78abf836de6890f782f0dbbea1e8c896b4f242c414b28e90f`  
		Last Modified: Tue, 16 Sep 2025 00:37:55 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46abc70ad26df8788108749d65c932140c4e3a14a9ca1712fb8876341b48bc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277460991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65025766ed044a8a2d11ae9b03b10ceadaf5d2622045ff5683324fb50c7beace`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1f932bd3ba0911a5731af0980fdb6950b5231a9b18895c1f007a292559706b`  
		Last Modified: Mon, 15 Sep 2025 23:26:03 GMT  
		Size: 142.5 MB (142458730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600c9cd2456aeb49e0a769064c7fc530fed37d7e2fc39d0bf2232a2666ad7a4`  
		Last Modified: Mon, 15 Sep 2025 23:26:48 GMT  
		Size: 85.4 MB (85357870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01630c2580cca0be3127339b1d90e75ab039de650fd12e88d4f018d56537b279`  
		Last Modified: Mon, 15 Sep 2025 23:26:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3540bd963d7b9c436a87d1b9178f51038e00b766a7c9118642d4d5d97debc221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163c274c400d85f0855d35401d77c87387632409078d190b73d080767b21755d`

```dockerfile
```

-	Layers:
	-	`sha256:1c12635c25f20c61bedc4f9de38ba987b66cf2e6597fb658396a4793e7d66c58`  
		Last Modified: Tue, 16 Sep 2025 00:38:02 GMT  
		Size: 7.5 MB (7494634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58fb966cf5b4ec1c1269495b85eaaccc6dc9fcaac63912f3f20a997934b9e66`  
		Last Modified: Tue, 16 Sep 2025 00:38:03 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:581450cbdb7ee2be3df5128b6c0648cd8d6801d85df92b6c35972e2c78d9cac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276909589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394e652c34f547e262c6ee2e28f60d2fdd688e2005947c424f36314254668ee0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df8dc61cee1bc6cfaa1fcae8dcd18fb431d0f530ac2e8ffbeb5882eb896e288`  
		Last Modified: Tue, 09 Sep 2025 12:17:37 GMT  
		Size: 132.9 MB (132853138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3831de25c927d65405ff5dd8832cfef6b9e3dd14c72a055e98448a8739bed13a`  
		Last Modified: Tue, 09 Sep 2025 12:17:35 GMT  
		Size: 91.0 MB (90951374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a51ce4eb29ca515bd33973de235162bfd219f4ee54e8fe6d3ca2b42130ee0`  
		Last Modified: Tue, 09 Sep 2025 12:17:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:44909a7ac18c9dd4c0acd5f009b2bfd11842d7e931496cf9854b6b5eb6c38b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a4df3fbb9b22922b3bd93c8631dba241b45d9a3a0b736031509ebf8ca76afb`

```dockerfile
```

-	Layers:
	-	`sha256:f5a9381cbb8a921fdf50913e22ce93d3673251024556707d510675ef7a14daa1`  
		Last Modified: Tue, 09 Sep 2025 15:35:47 GMT  
		Size: 7.5 MB (7490790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b791d134ce130d77a06c40460bbed886a7e820d56b434c7cc5350d2aca8b1e83`  
		Last Modified: Tue, 09 Sep 2025 15:35:48 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2d0cbf34e5f90575cbbe0144e833d0a24aca0120c5c07c60f0c9fbcd186105b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261475426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06c2245c109b34ed1e4489c56974e69f72dcdfd879a4ab276384cbe1edc581c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5c173fc2633ad8afcf6f0979f77c1c1c0dfe739ebf741748b555be75bac538`  
		Last Modified: Tue, 09 Sep 2025 12:35:01 GMT  
		Size: 125.6 MB (125622199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad12592f95cd4fe1afb9b9759ca14e541bdb7c8813cac0abae1051e049952de`  
		Last Modified: Tue, 09 Sep 2025 05:32:29 GMT  
		Size: 86.5 MB (86506256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7689bad2a44a7b3f6561a28af23692dedecbc46dedbd5f71bf8c32eae58c3121`  
		Last Modified: Tue, 09 Sep 2025 06:11:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7891642515f53aa21cb9c2acadf6262a616db998b715bf47ce3fa8289ed8c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9ccab21d3be5956e4a1ada5099ede02bbbbeb696832075b0ffb6a6dd019de4`

```dockerfile
```

-	Layers:
	-	`sha256:7c058975629c9a06133a9156176ed147ba199e59acc9b22df58d990ea205fa49`  
		Last Modified: Tue, 09 Sep 2025 06:36:20 GMT  
		Size: 7.5 MB (7482912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6940fda2aee536615ddcd179084fbfa5a8b6d16315b664db220a44429e2030`  
		Last Modified: Tue, 09 Sep 2025 06:36:21 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
