## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:01fae30b51d0986d9e2cc2d43578f798da9dc4ff49589df0080b8d360bf82eeb
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:541b24d35662277c5b4ee8546f975773df63f5d802deb818d3cf4ece84f7c4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253043651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160441d98b52d483b03907061fac2bb82554f5ef7c66aa96b5f76b74ad8a168c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:33 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5609493d2ecd019e755d5fa4e9841c858146c8c26df59645e047551ec760f972`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 158.2 MB (158166903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49e81991e44799439fee1ea4bb51cfa32c2d3067b9202ad0626aad87d536082`  
		Last Modified: Thu, 04 Jun 2026 17:47:06 GMT  
		Size: 66.6 MB (66642158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3978b88341cc58eb82c871f34138f49f25363a7b715be46ca93dc7797b5ba178`  
		Last Modified: Thu, 04 Jun 2026 17:47:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99457f46bb054bd3ca05e60a91492dce5e27113b8d72d74d21c93ef540cc6a56`  
		Last Modified: Thu, 04 Jun 2026 17:47:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aea70b2eeaec534d6db33fdf64cb2733c6951c95cbb622ef62741d36e5dad6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5544e0038461b4ca1a0c902e54ef055a9384b6b65f457ed9548e6a389ea13e`

```dockerfile
```

-	Layers:
	-	`sha256:42a0c9a5cc63441098973b02c94ccefd5d8d75f09476cfcf6863a8341196b5ce`  
		Last Modified: Thu, 04 Jun 2026 17:47:03 GMT  
		Size: 5.1 MB (5115833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a7d7812158464362351ec7e1984df3b1c1bd746d0090047de6ccadf29a2431c`  
		Last Modified: Thu, 04 Jun 2026 17:47:02 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40e3a5e32c4588cf7d361c16b1a5aa9f357fac03254e7c369982eb8050177c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251221170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317037a9a2bbd5d67147fa62f0eb341f59961c84f964adab9c027bef343d3d89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:46:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:34 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:34 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aae973b8255d28cba154cfb2e7d1109380624fac1eda17add9da5e76e7bbf9`  
		Last Modified: Thu, 04 Jun 2026 17:47:12 GMT  
		Size: 156.5 MB (156461250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460a17582708ad4b535e77b7a55b6f0939af2eed4f7fd4c1f5569fdc2b2a8aa4`  
		Last Modified: Thu, 04 Jun 2026 17:47:10 GMT  
		Size: 66.6 MB (66643833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecdbee5cfd4039fd3a70a93220bbaaa94162dcd9de2ee67612b577991b28cf0`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68976dda1df760d0a5059bf9b7b77043aebb0680e54da895c8a870126c15f8cb`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8714089b849aab64c00c13de6a86373c77f912891ec7ffefa3a2ed94c0774584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2327c8b02549e5f60b0c89a9ac30bb9f1581a68efaab36b2b66ebb5741929ec`

```dockerfile
```

-	Layers:
	-	`sha256:30a4415b172505eda30432c053e033fc30d504e826388389f554b68938b26bfc`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 5.1 MB (5121594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91080c6abf204f57bad0da4c6d2b6b7da2ede12aaca4f4748890f52223491c2f`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:60840c730c093a9fab30de697ac9ddf80b1ecac28b04a659ab52a002482f822d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262896035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270a27238e41d53672abaf580703518af115aa7f89893085edc9b3caba396dd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:58:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:58:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:58:23 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:59:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:59:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b5eac1372c58bf17e99c04c649b61fc2e6adc57b3b9da967a8850df068955`  
		Last Modified: Thu, 04 Jun 2026 17:59:55 GMT  
		Size: 158.3 MB (158343224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a4920934f69428ad5a43a330eca4bd9648bc599970c677d452276e6407909c`  
		Last Modified: Thu, 04 Jun 2026 17:59:53 GMT  
		Size: 72.5 MB (72476025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6656ba49bee3ed3b52da83c445ca5a27598396025d3e473739a2bef99afd9dad`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea18a6c09f4ecd6408aa54a7fbe3cada6a924a69270aeff2de05b90023272b`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d16985462be4ac7b897170bb75559ac2e7a9a6fcc9f0f2d097cc8dafb1aa849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08d61d7f4a7847abf63385e27dff3e56e79e81a2219e058a3b5109dfa1edba0`

```dockerfile
```

-	Layers:
	-	`sha256:63588ec93a920f90f03a7d2bfff6c913e43bc823f1b1fca3098910dc3cb0e610`  
		Last Modified: Thu, 04 Jun 2026 17:59:50 GMT  
		Size: 5.1 MB (5120991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb28b631b50cc4fe2f69cf47052ab0bd878aff6b67a9caf64fd28c2db1c9ea6`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8d1b8af91963194a97593972944b511e37fb59b32d7a9ee4499bb4f057614fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239730330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2364891b107dba46f37618f157268e134acc9126c3b9b328695347c79116a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:43:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:43:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:43:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:43:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:54 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:44:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:44:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:44:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:44:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:44:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8693092635138f62aa2560f0fec7170f0bafeb4baa2421d7b87ea124d3b1d41f`  
		Last Modified: Thu, 04 Jun 2026 17:44:42 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd51a5f49803fb052dfb49888a99fa4cf823588bb3f74ffeb61b479b7aabed8`  
		Last Modified: Thu, 04 Jun 2026 17:44:40 GMT  
		Size: 65.5 MB (65452344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea7ba37270525d7ef2dc644e6603cc7c9fca41a6556f8a7466c0bd1c2b70bf8`  
		Last Modified: Thu, 04 Jun 2026 17:44:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc87ce50ed671ef1e56f8345248af33abe248417d6ff81d39066c05e0fe410c8`  
		Last Modified: Thu, 04 Jun 2026 17:44:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:176263886c9071fad3900ef518dc4b3567ac25e9a71ce9a292266693452dd7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51d9e5eeee58d15745414f129819edaf719b8469fe969a815b49f0382463363`

```dockerfile
```

-	Layers:
	-	`sha256:b075f34d4b0df9201e7e1d1580882417f1634221a870c6babc782fa5a4dfb5b9`  
		Last Modified: Thu, 04 Jun 2026 17:44:38 GMT  
		Size: 5.1 MB (5107154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0a0b542e43b61a1caf3efebcad3ad7b74f48a71805e0d68447f56ff3ff0c9c`  
		Last Modified: Thu, 04 Jun 2026 17:44:38 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
