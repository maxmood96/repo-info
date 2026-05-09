## `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:1051c2568d0764eae15690dfc9ebf561c24f83e9ce9ec8d95dfea7df8be04ca2
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:89ecbe2f8ac65c8a4d211e2cb08879907bc7a032fa35b31a87efddc053417e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275542085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7e26528820a4f2aaab2f5ebb73f191792180f08e33fbfce1a9b9efb07489e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:16:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:16:07 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:16:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:16:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbfa9b9d5fa22c026c36c6c57c753dcba3bdcffec3e7f67c0cfef74ff59d503`  
		Last Modified: Fri, 08 May 2026 20:16:41 GMT  
		Size: 145.9 MB (145886194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0800b809bd1e35641d9fa8856bbb8b7092f3842ebee1e08ece63a9899c54d1`  
		Last Modified: Fri, 08 May 2026 20:16:40 GMT  
		Size: 81.2 MB (81166570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c4c0c877cfa14e1989c6c35260f924e0d9428fa1c42c9a5a5c932a3eb1602e`  
		Last Modified: Fri, 08 May 2026 20:16:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c561c392cbc2e5f96c737a4984859ecd33f49ec06190d3b00e8a52a556f4adee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02488a64987930d24b0c262f05317a10adef69b923f69f0435802e06d640eb4f`

```dockerfile
```

-	Layers:
	-	`sha256:589a9e9e35b87dad1bb0d83cdd3f9525b1b010ce69ecd960963b54e58ef64775`  
		Last Modified: Fri, 08 May 2026 20:16:37 GMT  
		Size: 7.4 MB (7398445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db73a20259677e7f891969522e6ebdcea6631f4f7719ccdec69ce688da6db02`  
		Last Modified: Fri, 08 May 2026 20:16:36 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96194ac66b74d6a0c5dbbae883262181537a03c62bf922bc7cce85a835a404dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272130367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d8d77829460fa00010e97e9a66c93df2ab72300932f918bcfc5f9cf010788d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:20:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ec7b60e0cccc29d9fbe85da1354a9f35c5ee0742d3b796f2bdc86a82b2149a`  
		Last Modified: Fri, 08 May 2026 20:21:03 GMT  
		Size: 142.6 MB (142582233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fd7af9ae793e08b91f1b4b0a858ee950969478125aeb1725d25b6e20be535`  
		Last Modified: Fri, 08 May 2026 20:21:01 GMT  
		Size: 81.2 MB (81174338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd274c2b2e1eefdb31b65851ff5e16dec4cbcb9d0332b0c311c90390a627d4f`  
		Last Modified: Fri, 08 May 2026 20:20:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8986918484f676e724075fca01aff7d6b5b470bb42404e8948e7bd0c1c113e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d567c16d930a994fc31c6442a21c43271173dbb88c7c997a21a0444a12fd6a`

```dockerfile
```

-	Layers:
	-	`sha256:5ce1e467cb80f1e2d43a271609941bedd117ad355b9828000209e8a02a894a37`  
		Last Modified: Fri, 08 May 2026 20:20:59 GMT  
		Size: 7.4 MB (7404826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ef3d7d442789f1ebfbe22a502e4c9467855075bffbc7c2b38b1ff2ff3c39ebb`  
		Last Modified: Fri, 08 May 2026 20:20:58 GMT  
		Size: 14.5 KB (14480 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0051c3908f8e3c5b0c9f0017cef6b1ea0bb39afb6605e4f302657f538db52b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272451846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72778bc77f28bb110ec9842af32b6a1482369e1e898ad9848338703187526564`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:25:03 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:28:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:28:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:28:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cbaabc187f4e33faa4937073e6b8d37c4b4ee8836b24edba986c27660880f2`  
		Last Modified: Sat, 09 May 2026 02:26:07 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c73b60e583446c127327278d758e13f5ee0177260a2018480251c0e2c73f1`  
		Last Modified: Sat, 09 May 2026 02:28:43 GMT  
		Size: 87.0 MB (87004247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb001a9a518e0bed60e27e6059ed07ed724d46e6f5ce433a4527640018a7786`  
		Last Modified: Sat, 09 May 2026 02:28:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8b458f7561aa13e8660cdada672f3ca56062f53012a7fcd0e6cd4258f4a18f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f93eedf81b5c3c16db313b64284a123a331522b1b60db8fa53ddf453b65807`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd2392574400405d63b0dcc8779aefc7eff3445eb893b1923754621e756dc0`  
		Last Modified: Sat, 09 May 2026 02:28:40 GMT  
		Size: 7.4 MB (7403046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46918ec48c71814d0c747db219eb4eea269f88e99303fb0309568398f0d0e9e7`  
		Last Modified: Sat, 09 May 2026 02:28:40 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:48a52d349495aed9f68429c4f27f65aba4cb23d66dae7531708e9d460f671ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253780351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dd7d41de27e8bc7a1d6bd87139dd22f3d77f99216363fb567cbdcac5341fd6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:13:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:13:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:13:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:13:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:14:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:14:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:14:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d441456f804e562a72712bd8e239bf084021a4f0e7270d943ec1bd8515a87c`  
		Last Modified: Fri, 08 May 2026 22:14:37 GMT  
		Size: 126.7 MB (126651743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a07493c94d36fa17f2ebeff62fc685db40288a3274024a32b9f229eb12d126c`  
		Last Modified: Fri, 08 May 2026 22:14:36 GMT  
		Size: 80.0 MB (79979941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c3537702da796ff8c0c99ad3a5172d33e3968abcb025beaec27f3989218d33`  
		Last Modified: Fri, 08 May 2026 22:14:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f39d2601319d883f4ad282c3f28d2a05d030dd7a94699521277f3131d6b5b183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821d85e1f715e34d886538e5f31a1a6af054e9629e98d9bc8faab4e6394b03a9`

```dockerfile
```

-	Layers:
	-	`sha256:bf616c34dc838cbee9852e58c8b2fecc59758c9909799e01d2d1dfc76afd7de2`  
		Last Modified: Fri, 08 May 2026 22:14:35 GMT  
		Size: 7.4 MB (7389768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:335817b6553a0ed217d57ef8cf52cfa22d1da448b5e70c78091bd6e2c13dc543`  
		Last Modified: Fri, 08 May 2026 22:14:34 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json
