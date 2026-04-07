## `varnish:fresh`

```console
$ docker pull varnish@sha256:3b6dd383092bf283d6eb94219dcb69dca0b6a9d4655ee978435d27568972b3bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:2093bc9e8099832040cd9901d04373dcae733ac4244e36963767a58591b5a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121020503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c183a53828c4b8bd28d7f78480c95b9503aa3b64ad8341c6cef35feaa560a66`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:10 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:43:10 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Tue, 07 Apr 2026 01:43:10 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:43:10 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:43:10 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:43:10 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:43:10 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:43:10 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:43:10 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:10 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:10 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 07 Apr 2026 01:43:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:43:10 GMT
USER varnish
# Tue, 07 Apr 2026 01:43:10 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085135467531374aabe1fce02981b1380113d31af547167565565e59c37984ad`  
		Last Modified: Tue, 07 Apr 2026 01:43:24 GMT  
		Size: 91.2 MB (91241984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26595b62ccaedb95dca6f3aa3af68e6c4b73ffed0c5c0b19ac9f49a4eef8fbd1`  
		Last Modified: Tue, 07 Apr 2026 01:43:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36accbc6e159a944753cc5cf9df85c9b276a2b3a9635cf18fe3a3dda5932b21f`  
		Last Modified: Tue, 07 Apr 2026 01:43:22 GMT  
		Size: 1.0 KB (1005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20467ad1e4be47fb995ded7130aa453920ff93c331ef350813ae4927be31399`  
		Last Modified: Tue, 07 Apr 2026 01:43:22 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:187ae8dd4441fd2c8d249a8bdd59687e93d23d7583dd388630617c4ebd3cad28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36d90c7fc141f0a9cce7714e4d90766b6570c1d6a4c7a5b9ad335ccb88c637b`

```dockerfile
```

-	Layers:
	-	`sha256:6c7bc47453e8eb2c482824ee8909d124c454c08a55ee7c34ffe92fe3da3428b4`  
		Last Modified: Tue, 07 Apr 2026 01:43:22 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1f645d7a6bf4beeb3739fa76bf6d1f638bf1c22d671a8b8a71dc20b5bd0c9f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115018790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f81ed841cc3f2ed34ee7cbcec7cddfff69e2d9acdedec9b64e6e6e74876945d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:47 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:47 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Tue, 07 Apr 2026 01:45:47 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:45:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:45:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:47 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:45:47 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:48 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:48 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 07 Apr 2026 01:45:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:48 GMT
USER varnish
# Tue, 07 Apr 2026 01:45:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:48 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd13ecab8149610236a45a9b5f15744e3b74310846c59a706a465b318aa706`  
		Last Modified: Tue, 07 Apr 2026 01:46:01 GMT  
		Size: 84.9 MB (84877353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415602245747d85c3f67217d8bd9aea878af889fe3a3d428b9c52ec7a31d1edf`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b86e02ffc45237eeaecfae39e46de2d53cba4d71bc73a42e029ec846249471`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69bdd691f71f03606b6e27b9c83ab1e12641c066a034e0f40e555f564c3dfa4`  
		Last Modified: Tue, 07 Apr 2026 01:46:00 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:c4b95efd75736771e2f7f23468abc0336f9c0874543a160271f101e3757b17d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9703ffcfe6e1dbbf23238e7d2a6998c81f8291083cd602bdce842b8337ccd0a5`

```dockerfile
```

-	Layers:
	-	`sha256:bd03f918a6165c0a27e1b0400cf1587d759da0e6982c457c85e542505ef8ecf4`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json
