## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:7e5739a039909bcc29f0517ef19e4e381bf7892dab4d35aae94602a246837b4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e2b744f0cd37255730d4e42cf1d50778a602a95825b06c89d23f4a822921968c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190036045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c0d92a23610c89e6f32c6ff182035590f15d72cb4189818e39b6a7c5f0c32e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:13:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:00 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:13:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:13:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18eb531585f80630785cdb6193cfb62a9eb228fe297de6c6fd484e4823f50f46`  
		Last Modified: Tue, 07 Apr 2026 03:13:35 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ac3abbff28a9c1f8351e32022a846d6a3fbdb09e3d35adbc5cd5008a5e5f9`  
		Last Modified: Tue, 07 Apr 2026 03:13:43 GMT  
		Size: 85.6 MB (85567449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee1441b6826b4293e5707fec876d213a362985c434b806de5f473719ef338d7`  
		Last Modified: Tue, 07 Apr 2026 03:13:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:70b17fdac94dca306e3fbba1ffab82d5b52fc645d59b33aed88b9cfe9c044fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752e2315ed8fac44133f59fa1cccb41e584f76f8fb055d7a72804cec8f24246a`

```dockerfile
```

-	Layers:
	-	`sha256:3846b841d6a4fc318096470f74892a1969d97c50c5f86ec416985e9e97efbf44`  
		Last Modified: Tue, 07 Apr 2026 03:13:41 GMT  
		Size: 7.6 MB (7591654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f852cc0b8ac753e05c9a1434b2c5de1cea9340faedb191c37e3fde1309648b5`  
		Last Modified: Tue, 07 Apr 2026 03:13:40 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1990a5177503499108b16da54d652bcbd3734c51c36b04ab514c1557f72457cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189300155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6cf57895399db81e90c431ce924e7f3f3d39e4252cfc8b5e423639ed10ef5e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:23:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:23:35 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:23:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:23:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f2fd5891d7b0199b8dc0ab4ed5546bfb39148b803a29a0e87c2362940a628`  
		Last Modified: Tue, 07 Apr 2026 03:24:16 GMT  
		Size: 54.3 MB (54251617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265bdbcf809dcb5b816e8c5a5dff2f34c095c561db1cb849a2301841ccff9c52`  
		Last Modified: Tue, 07 Apr 2026 03:24:17 GMT  
		Size: 85.4 MB (85382637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914271d8e2049160b813adaad4adf4e2504405926f4eff8ef29ef0f402bdd8f1`  
		Last Modified: Tue, 07 Apr 2026 03:24:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:17b4247829bfdb44eae57234d65e8a915ef7504acb05ba096b29d18b076bbbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9ab7ca9b81801201ef09b92dcc1e53839b178d8b874db2b3ae11e61007bb0f`

```dockerfile
```

-	Layers:
	-	`sha256:ef0f3109f624db096f816a6066366c2bdda72064eaafc8ca15b9cbba223d1e56`  
		Last Modified: Tue, 07 Apr 2026 03:24:14 GMT  
		Size: 7.6 MB (7599384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7de1f5a7eb3158ecd4625488129fd0c545b7d5ed5eb2a29d11a1a5cfd36414c`  
		Last Modified: Tue, 07 Apr 2026 03:24:14 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:044ab996129ee3787b0b3b22c2d32d61a7011ce56d306e66c272fc3d4061ad0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196756684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1a460b74b9f6620f0ff05d58806b136a5183df996e92a39cfda9fe8e5f7aa9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:08:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:08:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:08:41 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:14:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:14:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:14:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4e66022f0a54019718e5fb82aff975c8ae1279a587e803dd7d8da942e46b2`  
		Last Modified: Tue, 17 Mar 2026 18:10:01 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cc144117015cbe7fbcc5f528fba201f57e86b454481c54882894ded886c6ed`  
		Last Modified: Tue, 17 Mar 2026 18:15:28 GMT  
		Size: 91.0 MB (90987312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40fd21a39c957d198635b7b649f2b7001864d9b31727d383604732947bc8dee`  
		Last Modified: Tue, 17 Mar 2026 18:15:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4619f01d85e56224e33b9bd907dc84f7b4eb8c8e30da48927888f630adde46e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecc0990760058ab4f99c4b9a9dc37e075dc55ff14fef4190e2d4b28a01b2989`

```dockerfile
```

-	Layers:
	-	`sha256:90d8253a1cff1a45387014c3191416a585567c27a03d66ce74eaf05f441d6ee3`  
		Last Modified: Tue, 17 Mar 2026 18:15:25 GMT  
		Size: 7.6 MB (7596670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d13afc1cac2187fc410a519ae5f74de09024af66b89927fd80099e0aab7091e`  
		Last Modified: Tue, 17 Mar 2026 18:15:25 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
