## `varnish:latest`

```console
$ docker pull varnish@sha256:7146c8185a24b42d2233bb669b86fea12c1623dc922cc950efee17ba3a9b8921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:2f459717bad8b2b08fbf29c8b74f2c22a056c3ee69f17ca2678bccf411339c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121020566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa9537475cb0751c7bec4b57410e6276d332e4106b2cbc9a867b497c190b0a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:25 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:25 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:25 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:25 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:25 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:25 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:25 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956defc67a0580f9fd9ee9407db7c652c7ae707204582808de58228c8154abdd`  
		Last Modified: Mon, 23 Mar 2026 21:12:41 GMT  
		Size: 91.2 MB (91242179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bdea834e2af1aac140374d19b13f1fede3f60320c6365d7b7f5c55a0496c47`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43ba12a60fced427e2753efaaf818565598fc7b189b0e4c718d8c32fd2a0c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc71a769554ee2326e001a2f67c5e49424a5debd7c04b516967a29caf40a855`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:59feb0220565bbedaec23456b16c70c5403706af9c750a9c2bd165c38b49bbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab06dee630f531bf1ff657b84ea07c794fd29b65a1621ef4fcad646d20f8f6`

```dockerfile
```

-	Layers:
	-	`sha256:f10bdae9217fdc56afbf0f3fb942d0bd47c6fab87b3b92f83a7ab736aaad812e`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a50418e84d3a7744da85152619b0babca188f19eccd3354552dde8cdecd98f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115018223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb34cdfd366eb7d518256e6b50ae5a6af0bbcb45a9d3948d8aff09008633650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:34 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:34 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:34 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:34 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:34 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:34 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:34 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef81572ab25406c274dcdf5f919e59349d81a2ca4799bc60f6c1245e9b4e8`  
		Last Modified: Mon, 23 Mar 2026 21:12:47 GMT  
		Size: 84.9 MB (84876921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecea7934d0b71ae0729994a89929966fc2a9852f06c121fcb5ed212068cd5e`  
		Last Modified: Mon, 23 Mar 2026 21:12:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf1775d15b64385d723efebe785407fab2d9711d03b62e45625f1f0aad37c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb348ae1c19f498939a0eea32a13b1a3133e6a4d9d3861f043b9de89e36ed34`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:1b8dd378d06ce571a5f031d9d126933149a1af5d3a5fc61af35b00ce4fc5deec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553cc8148a431217ceddfce685ea8faec17906db96d1cee2e69d89f141db92ec`

```dockerfile
```

-	Layers:
	-	`sha256:b2edf9e74c2fffe31f33d731559e82ad854cb1494fb777a76ddb4dac28cf9e0e`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json
