## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:e71496710cc31015a140fbdfafedace9e0ce5bd08cc0bf8c4cecafec3cbad2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1afc11c93050d6884bd1da78e5bffe0fb96b0c5c9bef9e40bc1cac3ac756e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279505524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3216c63b22ef9abd4ae410404bd892940cc930758222e4c76489d8dc3a5843c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c74f1da4fb3767605ffdedff4c5e189e95b904ed1c49d437675f15a60f5c704`  
		Last Modified: Tue, 26 Aug 2025 17:27:29 GMT  
		Size: 144.7 MB (144693288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed826a9fabe379a05180c5aac954e24795730583236804382a6a2c218ed648f`  
		Last Modified: Tue, 26 Aug 2025 17:27:31 GMT  
		Size: 85.5 MB (85532912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd2f327530f8ffe44c10db07d500152d9f069aeaf07360dde4f501c75843b7b`  
		Last Modified: Tue, 26 Aug 2025 17:27:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a43f1f71ba87ae3c49c2eb9c084bc8c387539ef992c4da67ec64ebdc768b5`  
		Last Modified: Tue, 26 Aug 2025 17:27:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:61aea864ee4e660449ccaa6af6d96339ba768dbfa26a573c5e8b701de512b060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec611ce09b2258c9871a15c51d300ccca8e85f82e6ee47ef45f3675adf4f6b3`

```dockerfile
```

-	Layers:
	-	`sha256:271e49b315821311e334667681fc720f173fb9ee52cea8677d5de73cc13d4c7d`  
		Last Modified: Tue, 26 Aug 2025 18:38:49 GMT  
		Size: 7.5 MB (7462221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dec4449864070fc16bcfba85e78376bc49323232a7fe5bdfc780f7fe143297b`  
		Last Modified: Tue, 26 Aug 2025 18:38:50 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc262fac446336a4781f7cb2d6a3edaee6cb24759dfcdc59637ecc218db881ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278541184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bdf500773e7103ca84ee77e21c3e886647cb1fa49122ca86140f6ec575c565`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1b4924db0e9a6507273f53942c071f009dd0878c2430f6b5b0b67f21e1720a`  
		Last Modified: Tue, 19 Aug 2025 03:42:04 GMT  
		Size: 143.5 MB (143542131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05db609fb51f2324e9acdeab42b7b5d75aee45c26373daa1515d985d3fd907fd`  
		Last Modified: Tue, 26 Aug 2025 17:45:16 GMT  
		Size: 85.4 MB (85356406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292a988e9c8649e6d7a10a728315f169a7b42961205082e7d9b38f3c1f99e8e`  
		Last Modified: Tue, 26 Aug 2025 18:38:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226399e1ebb75e73c7dc2d3e96470d76f7a4629a3a624c1329fc6f3ae74ca03`  
		Last Modified: Tue, 26 Aug 2025 18:38:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a0354c57e90e68113e698558634d11f8ea415c15e6a259f581a8a3acaa01a14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13e630667b60776bf1b23d5eb5744e0274147187d40c008b4107fe8ce257f22`

```dockerfile
```

-	Layers:
	-	`sha256:9cab88b4e9ed8f1957501f050811b6169b53acd278f887f54f6f27f18b4bf392`  
		Last Modified: Tue, 26 Aug 2025 18:38:57 GMT  
		Size: 7.5 MB (7469251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2fbdd5ab8d31f28380498e741773790a7b136a396fea1833ffccfe203e95b5`  
		Last Modified: Tue, 26 Aug 2025 18:38:58 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b0879540dddcd55dbbea37dc77aa4bc5f812ca093612588ed8eaa440127a21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288417727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9938387e3c53b4ff6730434127286d041a6d09ebfd6b1f90fea8983488b1b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5096f4531428918861fb2e9c0966a5ff7b6e852e32764913f3a77fdb5d16a0d6`  
		Last Modified: Sun, 24 Aug 2025 02:07:43 GMT  
		Size: 144.4 MB (144372854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea8a03eb35599ce7b7a3e8915476b84cde92615e3921a0f772632b4e9bd6e81`  
		Last Modified: Tue, 26 Aug 2025 18:01:04 GMT  
		Size: 90.9 MB (90940443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfab0c62332a53bce027b48e762792876212411be87c1c277d1fdd0695bc6391`  
		Last Modified: Tue, 26 Aug 2025 18:00:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca8021777bf4e0d0f27fd4005137b247fe2a261e8613aebbd4e497fcb9d54d`  
		Last Modified: Tue, 26 Aug 2025 18:00:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:12a5080ee4f4d1cd5600888351bc5cd557e099faa464c76a452e44d61e1caed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ce30b972a1ee6050d4da1de8c0581f7a229ef72468e5c2350aec960bc5edf2`

```dockerfile
```

-	Layers:
	-	`sha256:74d5e6d15cca13051f90fbad7c972056a5b43fb0c30cc2733eac6c48ec76473a`  
		Last Modified: Tue, 26 Aug 2025 18:39:04 GMT  
		Size: 7.5 MB (7466640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d483c83d30ac5cf79ed8e07c2fc42edf14b8b22d0371fed46c4e988d18c30d`  
		Last Modified: Tue, 26 Aug 2025 18:39:05 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9fae8e961b5a43698204454400f00b20e4ada1e36ad3275746f0813667384707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270667409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded1a965ab174ec559002b8619d2b143527239a3ddbd6e7363c1ed7045d9cb77`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0498801f7d069ee03e6b4b2295a44eca76d9f1c80a0378ec99d41a263986c4`  
		Last Modified: Sun, 24 Aug 2025 02:08:04 GMT  
		Size: 138.6 MB (138575686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b22965ffa1049b562219d323180dafd68065136bd8d5522253bb37843b15b2`  
		Last Modified: Fri, 22 Aug 2025 00:26:27 GMT  
		Size: 84.3 MB (84326375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b088d32c60d6e843eb523a40674dba96638560718a626671719365e191f35fbb`  
		Last Modified: Fri, 22 Aug 2025 00:26:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe0cf12a221d7064c717b7aa409126bd7c93cb6143b97b48992db8d704570d6`  
		Last Modified: Fri, 22 Aug 2025 00:26:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:98e73e19551059dde72b58d95a5268da2b21e31fcf8584659608b71ff8b9320e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956db68c6db6fa9e3c1f5ef00fc82a17da7892a90de878254ca83df02b7dbac`

```dockerfile
```

-	Layers:
	-	`sha256:65ecdd0e2b048233785f05f5330ce4c213aa4b1c70bde9581a328baf330eb17c`  
		Last Modified: Fri, 22 Aug 2025 03:35:57 GMT  
		Size: 7.4 MB (7448215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4abcb5dda3d899e05539eddc020c3791bdb63d722bf7b171e3e462161cfa5ce`  
		Last Modified: Fri, 22 Aug 2025 03:35:58 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:656dba6e6b330acae757dd7384b9459d9fb15083079826457eefb6fc95949ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270473929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fea1a3f5000ed7c1a0cd0524852070d55108a193dfa7bbb9e6451ed9bfea59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef58001aee7acf83166d5ef416f4116fc450dc5d1056018e93ccc35ce853d4`  
		Last Modified: Fri, 22 Aug 2025 18:11:43 GMT  
		Size: 134.7 MB (134724432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4ced70cca78a2f20114e2d49e2d95e2703783383ee627aef814de94e2a97b7`  
		Last Modified: Mon, 18 Aug 2025 17:44:13 GMT  
		Size: 86.4 MB (86403290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30fd8c436f06876e830d3cb3f24d1870d1b36a7a90fe1260c9765f269b67242`  
		Last Modified: Mon, 18 Aug 2025 17:44:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b2f514d92a0b05fbee00fbbe3762c49388466809d50b034044c3dcda9857b`  
		Last Modified: Mon, 18 Aug 2025 17:44:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f3e1b394204f6d29e318d1fb55bd05454e29ec1d6ec893bb94105f6344c0b756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39655b6f7e2e5305628ae0a77744fbfdfa37bc27daa83ba33c69e5d1e2db1fd`

```dockerfile
```

-	Layers:
	-	`sha256:1b6e0f7362c514bf61924128c65a1bb40d972258ecf2653bc5ea5b81a1d01d8e`  
		Last Modified: Mon, 18 Aug 2025 18:39:22 GMT  
		Size: 7.5 MB (7458143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8350fe102acbfbd0dfa0e25f4b8b854d48e32ed195be3ffa8df5dcb2d688afe6`  
		Last Modified: Mon, 18 Aug 2025 18:39:23 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
