## `varnish:old`

```console
$ docker pull varnish@sha256:93ca8d2761bcd808aa149ede62ffb69fb9deee33702c3a985ed1bebf99fb9e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:b760a4d9e7deb6fb6928e857937ec45d7bd809462d9f3aafca2f47749808926d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120267305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a6f3777a38215bdd67ebc3ca379916aa07042af7550877a8311149e999868`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:14 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:38:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:38:14 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:38:14 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:38:14 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:38:14 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:38:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:38:14 GMT
USER varnish
# Thu, 11 Jun 2026 00:38:14 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:38:14 GMT
CMD []
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da9a79c67eef4921db9588a7fa2053bd00d1fb99c4adffe16774b5b3d988ddd`  
		Last Modified: Thu, 11 Jun 2026 00:38:28 GMT  
		Size: 90.5 MB (90478782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc13c1508b2be37c7ceea3566491eb20460bf597204ecf892a01a8411beb6e`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c7abe729a644a60ebbfc9fd8234038e402b912ba71beae591d1aae0ed9ca1`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34403bab4b524d1a81bbacb80bc88c649c8a27df3d8fe7fd801f7b194b3eae7`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:38fc5afa7f13b3801c2c1a9c9cc04e739ac9e9fb1ed297af5fd882db38051c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb94d4bf7670d0bfa9278211d47183e5de9e07f03f2a351d1f8680856ccd774`

```dockerfile
```

-	Layers:
	-	`sha256:8ed30f1a836dbc9e4875ccf97fe3505d98ef18f3ecb1a6777910d23926af85ad`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 20.9 KB (20869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:37af1a0ef9eef90e018ea1ce3bdcc0bc765e28f07573b8f5f96b572864a449fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114257327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12b12aa1a8aeb7f0dc002335617be3daea6c39c30ec344bc9bd9fe01696d6f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:59 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2-1
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Jun 2026 00:39:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Jun 2026 00:39:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Jun 2026 00:39:59 GMT
ENV VSM_NOPID=1
# Thu, 11 Jun 2026 00:39:59 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.2-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Jun 2026 00:39:59 GMT
WORKDIR /etc/varnish
# Thu, 11 Jun 2026 00:39:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
COPY index.html /etc/varnish/ # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Jun 2026 00:40:00 GMT
USER varnish
# Thu, 11 Jun 2026 00:40:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Jun 2026 00:40:00 GMT
CMD []
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58db64060edffb977091268464a3f40da9f797a6da82caa2426803a4022e10b`  
		Last Modified: Thu, 11 Jun 2026 00:40:13 GMT  
		Size: 84.1 MB (84105671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf2133883e29ca2682f4c36d0a73cc7d4b4c746cb2bf320dadc331389c58d3`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61016503c5f7c6c73f7fb3dc32e7cb0c599639a95b9aa6701f82f269df06409`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6289e570503f41585a8a5cc6c38c730e1db5fe15f722f4075bf7554db5c19`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:ddc0f89310b2142564a864822b963ea1fb5ec76b670893c8a7958690672c32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d94cf5d59545de715ace5a02ac511a5ac631c66f7d6aa3ec176e758ea3cc25`

```dockerfile
```

-	Layers:
	-	`sha256:c62198045bd7091b79cad1277652d338bbad606f7baaefa91e4f429f3248f71a`  
		Last Modified: Thu, 11 Jun 2026 00:40:11 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json
