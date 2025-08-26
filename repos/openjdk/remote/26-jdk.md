## `openjdk:26-jdk`

```console
$ docker pull openjdk@sha256:9889bdf7f62bf7e1e7a2716b2b790ab3dcbb0ca059713285d55c5c90fa761164
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:8c87d265e9b5331b8c3cf49741339d8611b6719bec31fa8216bb6a842739e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310583489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31546fc0d41c868eee47c4200fc969ab61b4ca48b283cded0ca95c45773aa912`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c69276785d440658cc7c706b1c14743d4dae8151373026e372596ff83da2a`  
		Last Modified: Mon, 25 Aug 2025 21:26:37 GMT  
		Size: 38.0 MB (38005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daab9091392d98034b0ff1a0d0d636270de1e6044b33c31bbe54ca5b5f2e4ad4`  
		Last Modified: Mon, 25 Aug 2025 21:27:02 GMT  
		Size: 223.1 MB (223081409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:7a581a59fa9305feacf4d84b68a38afdc0fe9cf546771a5ef9b914bf19d7d5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01ed90bde53bbb3f810ec4bbe0a2849bc2194d862ab8555c13bc984def86add`

```dockerfile
```

-	Layers:
	-	`sha256:3c697954f5c32bcb3b8c7f8f85069619d92d5798e53bca30b5b118ab0e3d35ca`  
		Last Modified: Mon, 25 Aug 2025 21:23:51 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efffc3e94d1412bac89b955b6d83e3df7625d635c88d021be4307a07ea25d612`  
		Last Modified: Mon, 25 Aug 2025 21:23:52 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ff89798e17ae589cdf81d22712b00f970f9cd03f37fbc22a1af0aaef32128d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307465032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538c56065c43974c68d24c27f94b65c90017bce006c6bbf486743b3b324ee271`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f251bedb6d0a7854cec601a06650a41a8800628c25948fd9b15b8018354d6f6`  
		Last Modified: Thu, 21 Aug 2025 20:15:43 GMT  
		Size: 38.4 MB (38406411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9fd6628c76e574a204d4d6720a32dd59a95911c00ef7249d109f36af8c062`  
		Last Modified: Mon, 25 Aug 2025 21:30:44 GMT  
		Size: 221.0 MB (220971898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5344b9da1e0461546a1dd83e3177fa6167eb4b770fd068395bad3dc0afaf3637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ff9082c795d3ccd633103d76c2ce27d975266391e868903db7feba6094ea8`

```dockerfile
```

-	Layers:
	-	`sha256:58299953a37202d113285c2c1e19e7289beee1ab1b547f418681bb6b7eadd842`  
		Last Modified: Tue, 26 Aug 2025 00:23:52 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8ef1aaf55c85b7782df316f1a754c9690827cf56ae071947f8d0b831fbfbbe`  
		Last Modified: Tue, 26 Aug 2025 00:23:53 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:775acd02a7f2bbbb3590c8bea58ff76b4b6393586f586de6cc1f88aeacd1ea7e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718711149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374a8d2bcbf99bb0e03cc1349619f242fccec60e22ab4343b7d67d37c7fb2636`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 25 Aug 2025 21:00:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 21:00:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 21:00:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 25 Aug 2025 21:00:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 21:00:52 GMT
ENV JAVA_VERSION=26-ea+12
# Mon, 25 Aug 2025 21:00:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_windows-x64_bin.zip
# Mon, 25 Aug 2025 21:00:54 GMT
ENV JAVA_SHA256=1998fd0551258ac7c1815fdf5d70e77c4d82759755d956bcc599f16636fb4c7e
# Mon, 25 Aug 2025 21:01:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Aug 2025 21:01:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bc0e5fd26b11245901156f7160c8d412c98134fa6300162f30b68404f60699`  
		Last Modified: Mon, 25 Aug 2025 21:04:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0fc79da67ddca75a21fe7560bbd65f9940bbcca88192ffa6874698efbc5c13`  
		Last Modified: Mon, 25 Aug 2025 21:04:49 GMT  
		Size: 403.4 KB (403356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ac11e60f6e6c4bba9ccc483e5c322b12c45c00549544375eeb7df6a20dbe6f`  
		Last Modified: Mon, 25 Aug 2025 21:04:49 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6affdeb490f60585e423b9b63a4403f6a5302d3f5c68c77a6b583760b74d48`  
		Last Modified: Mon, 25 Aug 2025 21:04:51 GMT  
		Size: 382.8 KB (382779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6340ee96a2b42f83657c450e26975abb4fe0ca7513e7093d70ccb723d90c250d`  
		Last Modified: Mon, 25 Aug 2025 21:04:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f651d5c52128165bb104469cfefca3704c9b1bc54fc508b3e4b2eb5fd8fee8`  
		Last Modified: Mon, 25 Aug 2025 21:04:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877992c07fb0cc14789f1839e473fafc79c2759372ddbc0868a280db49dc4c02`  
		Last Modified: Mon, 25 Aug 2025 21:04:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3573a0f7d9e8ec4c512f25bbb099ba131a22eb6d864cdc46d1a0b9230ac0e6e4`  
		Last Modified: Mon, 25 Aug 2025 21:08:00 GMT  
		Size: 219.1 MB (219086781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93665e9b679f0a08e5c90eafa070a721d4f06d4cfce3dcca8488a12732eeae9`  
		Last Modified: Mon, 25 Aug 2025 21:04:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:cb28f769a236bd2d3fd7bb94f14c65d3ed59fc90fc947b4ebb0efc40e76b160f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501437179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec7a09107e80ff0a6b1383be297ec7419efe1ac9851e1233aa9d77c12157a74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 20:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 20:55:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 20:55:05 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 25 Aug 2025 20:55:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Aug 2025 20:55:14 GMT
ENV JAVA_VERSION=26-ea+12
# Mon, 25 Aug 2025 20:55:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_windows-x64_bin.zip
# Mon, 25 Aug 2025 20:55:16 GMT
ENV JAVA_SHA256=1998fd0551258ac7c1815fdf5d70e77c4d82759755d956bcc599f16636fb4c7e
# Mon, 25 Aug 2025 20:55:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Aug 2025 20:55:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6db690a6df5eab11b3c2d5b2b8c63cb734052e63335bbf101606fea21cc85`  
		Last Modified: Mon, 25 Aug 2025 20:56:28 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cf5e087446fdcc85b769cd0ad070f5f58d7ce18f14c9adb18dd760d3e20d70`  
		Last Modified: Mon, 25 Aug 2025 20:56:20 GMT  
		Size: 355.7 KB (355704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1286033d8f4352e89f58b84bc870c7b6294c839f96e9ce98aaf771378b27f742`  
		Last Modified: Mon, 25 Aug 2025 20:56:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7856ee342197f4f3ad70a737f7b0e599d226fe3af6789addce4af0e2d3dc9f`  
		Last Modified: Mon, 25 Aug 2025 20:56:21 GMT  
		Size: 341.8 KB (341786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff8e7a332babd9881ffffbb6f0b977005583582926a912a855c74dade0be3`  
		Last Modified: Mon, 25 Aug 2025 20:56:21 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742fe53256007c4b516a868864d6519afeec84c40968f789abf6fbd880f247f5`  
		Last Modified: Mon, 25 Aug 2025 20:56:21 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67b10e01f8b8702e732b3dbb7d34f85f8b56e28608116d5c87e2f3b1d5d2087`  
		Last Modified: Mon, 25 Aug 2025 20:56:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b664f9d65e7d65e84f3a64e17e5671d8e01c125b401c4af16db85796b9eddd4`  
		Last Modified: Mon, 25 Aug 2025 21:08:05 GMT  
		Size: 219.0 MB (219040038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b9b3a4e3edbe87bd9cfc5724ba53b7f020466f6edd6c5ae28d9c435fc98ec9`  
		Last Modified: Mon, 25 Aug 2025 20:56:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
