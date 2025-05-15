## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:419831d8874a1075d0cde86bff8806e0f043de4a4608fb1512286a6efc0486f5
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:754b75dc2d4be7f8a043593183a0ce13bd2023eb04f2a371bd0d29db95ee4aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246113874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82727e7109b90f4b5de014a9a311b062c603e20585d1c1c27517a7d1d12f44e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Thu, 08 May 2025 17:06:40 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a9e6e9439e1e71dc15cf1210c05634bbd063835a1bd6b1be16383dd15dd8c`  
		Last Modified: Tue, 13 May 2025 17:53:52 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0953565df9ea772364f47d625ab43415aca16103446c7402b81c4421b76ec6d`  
		Last Modified: Tue, 13 May 2025 17:53:51 GMT  
		Size: 71.7 MB (71723965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d133eb9e49ded403bf070237c8128088486f27f87378038690cd234cd839580d`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ca2388017d2a92a2934c63bac990a79197f84328722a9df6aa9862eb0265cd`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0a3bc6b293ef821fc58bfab3afc994172c884a856ad12fe965f8327122ba38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b3a32499749fad62a81f836a701d7bc5e34ef948aeb598324a28d7a670828c`

```dockerfile
```

-	Layers:
	-	`sha256:b432fa5d86fb236abd67ce2111a47f0cddec0ab5c451aa6b47d0e490e025991e`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 5.1 MB (5066687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c129f46d097dc2b3b6bc744852685bc3afbeb20de6934a6feb9ce2140b94993e`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f709dc0750c67d9cc016b29b9b190b3629ed0599843be88904738c6dd077af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245290048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daaf34f1fd16a3ec768a1c9d8bec32bf02e873d1b31fcafcef295485f6750bd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Thu, 08 May 2025 17:31:22 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1862c5660d0d55c936747bbb44d2f2a5a6c318c406ceb110d2aac1c4519264`  
		Last Modified: Tue, 13 May 2025 18:01:43 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d7dac7317d6e16558e8bc9ba4e6d01bbf9dbda8a4cf1d851e7ccba061b5746`  
		Last Modified: Tue, 13 May 2025 18:03:26 GMT  
		Size: 71.6 MB (71646144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a0110d4502c8ec26b1a0d12b365d5e073b1577431825681f38ed8719f04463`  
		Last Modified: Tue, 13 May 2025 18:03:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f0e28c097e8252696ab8487b60904a2183948e4e6174d96135d188310ca020`  
		Last Modified: Tue, 13 May 2025 18:03:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f7032e52da44597110f15d945dca67b1467a385adf3f13428cc5902d433381d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc473bbb7d0622b9b1b698edf41767730558902480f19515f793852e9d47da81`

```dockerfile
```

-	Layers:
	-	`sha256:10be57bff03180dcb84d6a75fa385b4817ee55ecaf8ae189ca1d8c6549ce8f15`  
		Last Modified: Tue, 13 May 2025 18:03:24 GMT  
		Size: 5.1 MB (5072456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7331aa816c89115dce4ff1e16d18e9752ef13e460d4b09ce297b067a0d5a5cf5`  
		Last Modified: Tue, 13 May 2025 18:03:23 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ed1d126cdda007efea0b1c52e6601f47c1294ff19538515ae7878655e24a7dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255074308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e5bbe3cfb6d8de553edda067cb36c577e57f8df23d46a74dbc5a385cb86106`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Fri, 09 May 2025 00:17:30 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c71ca239809271676c3c02eaf9b6189c986087dbccce9fa3aca9bf1852aa9f`  
		Last Modified: Tue, 13 May 2025 18:59:38 GMT  
		Size: 144.3 MB (144280488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d3e5d2312eaf65ffb763c605d6829434d64f1789da9498b856349e90453004`  
		Last Modified: Tue, 13 May 2025 19:09:25 GMT  
		Size: 77.2 MB (77215089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a81ffa08b088b09a542c157639f8a41983ff76a8090201d808ffd951787164c`  
		Last Modified: Tue, 13 May 2025 19:09:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5471b5772bb9a7af33617a70f922481d6d24f7efb18d406264fb916b1643e3`  
		Last Modified: Tue, 13 May 2025 19:09:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bcb68b160ff34695f58fdbd68b1de7bff9380a88fcecfb7ed73f554c6cb9f6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85184100da8e7784856345c2cd73c7f7453df5493c61bfebf379a7ae5aaf4f7`

```dockerfile
```

-	Layers:
	-	`sha256:ff3524de8d3a46573397669a724b1b079608ce905ea99ccddb644886e5456623`  
		Last Modified: Tue, 13 May 2025 19:09:23 GMT  
		Size: 5.1 MB (5070896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc371b736a0f709a6c1ee4d1cfa26a2f23f7fcd92bb950c7b6edd6e305dd6f9`  
		Last Modified: Tue, 13 May 2025 19:09:22 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:00c34d975632fcb2b76c82a07e48cc3edb6877a3eb6b18110430fd211d06a9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237437143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70a689643dd9c98d297a27bb5fd4c7a095253236191e2f014829927f71632f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:facf81ceeaa2f81a0f9ef1ab66d52f94aba08977754588b2609aaf3106342525`  
		Last Modified: Fri, 09 May 2025 06:41:03 GMT  
		Size: 28.3 MB (28251718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe73eb42cc2635ac942e3dbc64942a805995a7c9330e4728fcf9f9491a2d8f`  
		Last Modified: Tue, 13 May 2025 18:14:54 GMT  
		Size: 138.5 MB (138492628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d623f1504315a8d46669c2445e7f2ef31f12fbc9f5211f4eb46e3985322b3`  
		Last Modified: Tue, 13 May 2025 18:37:15 GMT  
		Size: 70.7 MB (70691753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e24390ca6351f4aecaf05bf246d75e7e52dd4af6af99b55605a69e596293f0`  
		Last Modified: Tue, 13 May 2025 18:37:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b5c3d3701c4287c5f7ba98a018b3cc4ab249c245a2b1a7be113d6887a0b8d9`  
		Last Modified: Tue, 13 May 2025 18:37:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f6f9d2ed8c71acd01fd3886fca40db157ddb133c70e79f9adc55048d8ba3b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02704b160f96429e77567f0d7733e3b3f854ed74d72e4b6d648b53d4b5f833e6`

```dockerfile
```

-	Layers:
	-	`sha256:a780cc6baede5af92e51c3b0b265e15b03e5c62e4305d4b47aaf9ca380c2b194`  
		Last Modified: Tue, 13 May 2025 18:37:06 GMT  
		Size: 5.1 MB (5054350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8399dd5b6c31bbdc3d7a9675da1c7eab65aed29177acb957f8c49e75d2a725`  
		Last Modified: Tue, 13 May 2025 18:37:05 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4cbbed505e4cfd77dfc5ede74eef1bec6f3162ab4c194865d874d3d3b8731a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237313457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e329c560a0d839ed82b8721380bb4791976a6e2459b4fc3d34525ad5d7066500`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2efa8ce97d282fc76ea2985fc31102becef655447ddbf9bdd3209771347a0182`  
		Last Modified: Thu, 08 May 2025 17:32:36 GMT  
		Size: 29.8 MB (29825462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b674b6d2790c8572b4f337294d5779bf8394dac4c40b0e834eaff345e3fc45`  
		Last Modified: Tue, 13 May 2025 18:14:24 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3750763831b681d31709375b8d2f37a1e040c6866ca0e217ec22a5af700743`  
		Last Modified: Tue, 13 May 2025 18:20:09 GMT  
		Size: 72.8 MB (72813392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239cb4d71270e05aa3478b52ec841c57d19ae0e6e9d3f21ac20b67873bbd69f0`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bacfb4074269eadedb17671e5bce47bc419b4e806e5b142f50029f7e3851f02`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1162ccde9e9bc28f07562cd53d2184f48dbf42777fe628c545cb900741a654be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d21a03d44bbf6da2e94a8a0e00c4b6c9136ae10665e3e0ba32bd81c90c8de8`

```dockerfile
```

-	Layers:
	-	`sha256:eb58ac5e17a549ca623372a5fe0eb68b077c77818bf065567cc7b93995f4d82b`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 5.1 MB (5062611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc48267d1a8015d81cfa4df364728dda19db1e41109e0af7869a38529cea97a0`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json
