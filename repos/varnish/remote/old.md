## `varnish:old`

```console
$ docker pull varnish@sha256:5a858bdf9f58f3594068561a83c0118bbac4d33115fdcfe696b9848ac00fb874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:1d3f3e1488bdb098172a83e7a0945366aaf4758b24b546cd6228d0788ac0acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704910fdf8acb521b137eb1c582d117bf276fc9cdbcb63924cec65ad82d42cea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:43:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:43:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:43:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:43:16 GMT
USER varnish
# Tue, 07 Apr 2026 01:43:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:43:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c95874e0f344466754391b7814d464fefdc4ab8c4b1cd8b7212eaf12501a6`  
		Last Modified: Tue, 07 Apr 2026 01:43:30 GMT  
		Size: 89.2 MB (89191026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0100e77b0565c2bd21409eb5e342f7f50b720ef2a14c69445c1568676b2a40e8`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764fdc9687224de301a170cc8e83dea71e5a3cf3a409e55af1498ad2eca9f58`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5307540174c82b00c0ec9143fcd4a145e229bd752f225bc799c6e17b3aefd819`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:774b08e1fc8028fbe42b005ee640a70e1dfc8e39dd767b5767888bb2ed69b9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38f3dfa0f2f39666f75096a358de1673426ae8aa1947a3c848d1cc844ddf585`

```dockerfile
```

-	Layers:
	-	`sha256:3a275ad839eb9f637c806e0f07c2997954fca97d77056c69f76e3b7f0d8b1aaa`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:de8b7f4ac8eb159c3a54e4da0433e4738814f03d9ad2766f97bfd7572c2d578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d09b8db52da7ec70bdb708f0b250878dfe56901e65ccdc1f23fa01506706b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:45:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:45:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:51 GMT
USER varnish
# Tue, 07 Apr 2026 01:45:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:51 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6827838a7494d352d3517a378420f6f240e1c2836595174a325b46e7bbafed`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 82.8 MB (82838785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415602245747d85c3f67217d8bd9aea878af889fe3a3d428b9c52ec7a31d1edf`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60023cc98fb7529f68b7666443a15ea520e1e03ff0aae66a991639dba65b691d`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92c13a3e89c80bf3a497d8d05e31e98b647ce2f0b9e3c9aa5b637a0dc483de`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:261c213a261f10f93f4fb7a95462b9228b67e9e57bfc6da5fb7504943a55d127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2b5d729ed8071c671bde7dbe22e970e06717c24b3aff9eac3d95ff99387e6`

```dockerfile
```

-	Layers:
	-	`sha256:126cad36bd2a7055aaca0c9b6d346d2a079533d11cafd4c5cef693c7b32a46cd`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 20.7 KB (20671 bytes)  
		MIME: application/vnd.in-toto+json
