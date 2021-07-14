## `mongo:latest`

```console
$ docker pull mongo@sha256:5658ab179211c5ffccff5f28d2d937edeb1c35f879aac7da2b8a72d02c535fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:f9791f66c75cbc57908c95af316e5b5fa12cfdacc179fce3c5a5145021c6c9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244581829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196db23552390f39f699a15ec477c411d9cc69c3c8794c73a6e4197641313c4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 01:06:04 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 14 Jul 2021 01:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:06:13 GMT
ENV GOSU_VERSION=1.12
# Wed, 14 Jul 2021 01:06:13 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 14 Jul 2021 01:06:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:06:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:06:26 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:06:26 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 14 Jul 2021 01:06:26 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 14 Jul 2021 01:06:26 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 14 Jul 2021 01:06:26 GMT
ENV MONGO_MAJOR=5.0
# Wed, 14 Jul 2021 01:06:28 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 14 Jul 2021 01:06:28 GMT
ENV MONGO_VERSION=5.0.0
# Wed, 14 Jul 2021 01:06:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 14 Jul 2021 01:06:55 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 14 Jul 2021 01:06:55 GMT
VOLUME [/data/db /data/configdb]
# Wed, 14 Jul 2021 01:06:55 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:06:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:06:56 GMT
EXPOSE 27017
# Wed, 14 Jul 2021 01:06:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8490627ad476fc39c34e4117fe95181f23c0593c5939334f690c25267a15d1fc`  
		Last Modified: Wed, 14 Jul 2021 01:09:33 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d640de21f3bf1bccb594ae1a3788de970a320dd5c506685ddddb13af3871ff`  
		Last Modified: Wed, 14 Jul 2021 01:09:34 GMT  
		Size: 3.1 MB (3063668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4676d8bbe06cee8d0ab6acff7d9a319287a789dcd95864defe5419be03d50e86`  
		Last Modified: Wed, 14 Jul 2021 01:09:35 GMT  
		Size: 6.5 MB (6505798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33fdc30cbb092983846fd92465e892eeb6684e8391cc3b833f5980850b7e9c7`  
		Last Modified: Wed, 14 Jul 2021 01:09:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53109f095ceedc6db495547b88daf53fa0a33c7b5d02b8336c12409cdb0130d1`  
		Last Modified: Wed, 14 Jul 2021 01:09:31 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3df330e925b84235894428a7a97c6edd0f7e84501b9affb0dd5646cfd5305e`  
		Last Modified: Wed, 14 Jul 2021 01:09:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cbf2472323c0aa76b43eb46d89d15758d5cedfe6f47a89bcb10b6b9da91f99`  
		Last Modified: Wed, 14 Jul 2021 01:10:00 GMT  
		Size: 206.4 MB (206438295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d196d4cd5baca9f8a8829d2b160e5e72d65c9c060694165c9c2922a7c032dfd9`  
		Last Modified: Wed, 14 Jul 2021 01:09:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc46d2c7828db6d27b9901c34fcc76cee622be3b4d41dabbf9e61d64d583916`  
		Last Modified: Wed, 14 Jul 2021 01:09:31 GMT  
		Size: 4.5 KB (4478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:811f2b3406c8f29e92e08263f587ec8ddd70047640e452c3e80fdca47063cf51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237267174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed99c5be9d0b71cf14d474d895139e8417332920cb501729f9a6c401377c1f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:33:22 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 13 Jul 2021 23:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:33:30 GMT
ENV GOSU_VERSION=1.12
# Tue, 13 Jul 2021 23:33:30 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 13 Jul 2021 23:33:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jul 2021 23:33:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 23:33:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 23:33:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 13 Jul 2021 23:33:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 13 Jul 2021 23:33:47 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 13 Jul 2021 23:33:48 GMT
ENV MONGO_MAJOR=5.0
# Tue, 13 Jul 2021 23:33:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 13 Jul 2021 23:33:49 GMT
ENV MONGO_VERSION=5.0.0
# Tue, 13 Jul 2021 23:34:09 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 13 Jul 2021 23:34:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 13 Jul 2021 23:34:11 GMT
VOLUME [/data/db /data/configdb]
# Tue, 13 Jul 2021 23:34:12 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Tue, 13 Jul 2021 23:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 23:34:12 GMT
EXPOSE 27017
# Tue, 13 Jul 2021 23:34:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0566436151d6a7bfcb49cbc366b5ba571653a68dae1979813510507f0b568665`  
		Last Modified: Tue, 13 Jul 2021 23:37:25 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e35ecfc23ef3b8965133b69f802364d5921cd8275578e99ebc64e709465495`  
		Last Modified: Tue, 13 Jul 2021 23:37:25 GMT  
		Size: 2.9 MB (2913102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03a1be757b04fe0321c6b2dc153d150f21357471d616a43fd71b7fdd3012a2e`  
		Last Modified: Tue, 13 Jul 2021 23:37:26 GMT  
		Size: 6.4 MB (6406269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea0d006dcea6ae065db690271b288012719161d730fdb41f36389e0c4a6b06b`  
		Last Modified: Tue, 13 Jul 2021 23:37:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3641cc27fe99e40a4cfcd71de01f76ecc3f832a73a0baeacee292d57bbbc68e`  
		Last Modified: Tue, 13 Jul 2021 23:37:22 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748bfafaa84cc738e07f8080024936c5d43c85e283bc93ccca4c9ca7a534e552`  
		Last Modified: Tue, 13 Jul 2021 23:37:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4565ad280501ba664913fbe01800a646c33fa877aa2b2ec1488b20cb5306f4`  
		Last Modified: Tue, 13 Jul 2021 23:37:52 GMT  
		Size: 200.8 MB (200770516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edbbaac93ef818524f5a9ec9164659593eb15cb55e2ddfec3e4607bcd71e9d3`  
		Last Modified: Tue, 13 Jul 2021 23:37:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d9717ea6a831f15dff8aef701e21552acc8205dafa38fee0207aac9768eb8`  
		Last Modified: Tue, 13 Jul 2021 23:37:22 GMT  
		Size: 4.5 KB (4474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.1999; amd64

```console
$ docker pull mongo@sha256:f29cf811ea027d47b3f5340a1d5d63d782769c796c1c420995bfc841d1803c43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2873302372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec15f7149ae28b361ad54f2e2873c4e52589c9055d3a6c69ebae2ecf1fccc62`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 20:38:08 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 09 Jun 2021 20:38:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.6-signed.msi
# Wed, 09 Jun 2021 20:38:14 GMT
ENV MONGO_DOWNLOAD_SHA256=ede50e8f8d8c9d23a8ca2cc1c96cdb9bcc1f617930e8bd1d46f21d95d0b555f8
# Wed, 09 Jun 2021 20:40:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Jun 2021 20:40:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jun 2021 20:40:14 GMT
EXPOSE 27017
# Wed, 09 Jun 2021 20:40:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad0d495f3c090c8857d01c8c5c1d8808a0bd1ebe3acfc68cddc0518c316610`  
		Last Modified: Wed, 09 Jun 2021 21:05:12 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9348cb301dc54c9ee2b3f8272d11780555f985ea355cee0ce937d0cddaf45720`  
		Last Modified: Wed, 09 Jun 2021 21:05:11 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6903e6d82f07267bb25a20ef882109bed3163557a58cd437a2af16689aa9e5b1`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaf79bf9107c588c097d630b343f685f276e07697d8bb199cd470153d94239e`  
		Last Modified: Wed, 09 Jun 2021 21:06:01 GMT  
		Size: 231.7 MB (231707523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ff79e7a1c0d2cc43105f021997558851fa1b429b657840b2cb3fb7c94f9924`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c487450715e390654352a901925f1db5f5892e3953b8ace13a9355a429e6f`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5ec238c82175f83e27fc909d6ce4034997893f49209d2100d4225cb9acc2a1`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.4467; amd64

```console
$ docker pull mongo@sha256:b01b78e78ff15717c569d71b13f27bad07e0a54b9f22b7d338992aab78a52095
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6501876232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbf1160505acb0d2b0e89f9a079acda8bbcbedd1ce856ce14483d8e4e73a49f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 20:40:35 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 09 Jun 2021 20:40:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.6-signed.msi
# Wed, 09 Jun 2021 20:40:39 GMT
ENV MONGO_DOWNLOAD_SHA256=ede50e8f8d8c9d23a8ca2cc1c96cdb9bcc1f617930e8bd1d46f21d95d0b555f8
# Wed, 09 Jun 2021 20:43:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Jun 2021 20:43:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jun 2021 20:43:44 GMT
EXPOSE 27017
# Wed, 09 Jun 2021 20:43:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6562d39fa84cb30abdaf8ba85c49633fe3dbbbb574b420d3d6f0b6dcd84612c`  
		Last Modified: Wed, 09 Jun 2021 21:06:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632dffa8911cfd4ce0e581711217246f0acb2c9aa23c00d1665325ca9d01474d`  
		Last Modified: Wed, 09 Jun 2021 21:06:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d1a10881159fec53a734a20335f669c66ec8fad205ff18837714b08a2e57eb`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fea5282878f8bceeabdfa4eee9a3b15fa82046d07b73acc8bede72ed373e6eb`  
		Last Modified: Wed, 09 Jun 2021 21:10:53 GMT  
		Size: 236.1 MB (236139160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37d1edadef24c3d2d47473839335006c5e263b365ed3421f7da2ac8cf8d87db`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11529cee90aaa262ba14cbf27ff16a20766bacb7c7c673522446ebf8ae34b949`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c741f47ea5e251f30ac58630bf0c9d48dd7a1cc68e6394f1ad1c5dfe0aed50ed`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
