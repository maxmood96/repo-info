## `openjdk:27-ea-4-jdk`

```console
$ docker pull openjdk@sha256:f571a286710a97da8d72ec5f77d29624fb2e7fc2397cb8cd19776011af1cf826
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-4-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:3505074074a84c7dbc0012f87f1e09b6329a1ef1bd25708ca21a9286896fbe1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313522870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8de6e0aef7c0b87cdab25b0b9317be42bb52372705d6c752b80f2b23b525ec`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:28:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 16 Jan 2026 23:28:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:28:42 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:28:42 GMT
ENV JAVA_VERSION=27-ea+4
# Fri, 16 Jan 2026 23:28:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:28:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc6a75e130e02b91d0820ad93a640d7f28f2c23f23528271e3641694330c749`  
		Last Modified: Fri, 16 Jan 2026 23:29:15 GMT  
		Size: 38.3 MB (38295743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b663e32a2b97b41e16bcc868cae73292acd229e41299de4974acc748e85e1ecc`  
		Last Modified: Fri, 16 Jan 2026 23:30:10 GMT  
		Size: 227.9 MB (227912589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:16947f364a18f0dbea4ca24ab3e29483359bfd0cd5247fdce96233fa512472c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a94b742623575e562a9da324df26321e405a7d128885d81cf3d58dcfbe24a99`

```dockerfile
```

-	Layers:
	-	`sha256:fa3d99859f0e522da22063744c2abf00c9e3e261514f27209bb4986196258178`  
		Last Modified: Sat, 17 Jan 2026 01:24:20 GMT  
		Size: 3.7 MB (3655355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcaa7e1607eae2d1f1000eeacf29dadaa8cceb6db73beb751b42c771aaeb9b84`  
		Last Modified: Fri, 16 Jan 2026 23:29:01 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0408de3ff396d0b49fde7a77083846e877fac2090ec8371c3db1deded45a852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310435838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9eefa553d3100390959b76011ca25423ecdaeee9f50a7d0ceb5a916b295a11`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:31:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:31:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 16 Jan 2026 23:31:50 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:31:50 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:31:50 GMT
ENV JAVA_VERSION=27-ea+4
# Fri, 16 Jan 2026 23:31:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:31:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7099d6fad7d14a21ea13db57086b9cd7129cb7c247e916d93f12c415ab3c551`  
		Last Modified: Fri, 16 Jan 2026 23:32:22 GMT  
		Size: 38.7 MB (38697670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5895cb36439eca786b73f203fffd05652abca69df530950daa56e58eb38df063`  
		Last Modified: Fri, 16 Jan 2026 23:32:36 GMT  
		Size: 225.8 MB (225836265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fd102b1f2a1aa08e185cd23a078060b9cd3851ed5a76bc28a09b009f876bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8838c32b0a93b7e58211a596462f58a9f0ade110e694a1f363755c084cd5c016`

```dockerfile
```

-	Layers:
	-	`sha256:ff02396afc759f3c0a02db77c716dd898ff449e48ad70058568013d2a908d27e`  
		Last Modified: Sat, 17 Jan 2026 01:24:25 GMT  
		Size: 3.7 MB (3653045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86fddf70be616b0ff1166fa3ee498d2ea40eed418a837573054b417d400f2890`  
		Last Modified: Sat, 17 Jan 2026 01:24:26 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-jdk` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:f6fe9daecd84da6d1e1e691c171b9aa9685291b463b900847a006c98e2fa7420
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1720873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f65302859abb515129f1dec963ad4c304a2fbe6d247164a0eefd0394ccbb43`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:00:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:00:46 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 13 Jan 2026 23:00:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:00:52 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 23:00:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Tue, 13 Jan 2026 23:00:54 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Tue, 13 Jan 2026 23:01:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:01:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c348082658f8a5ab278a6856dfa04fa2a0bb282804f2a57c36436a6688e78`  
		Last Modified: Tue, 13 Jan 2026 22:58:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da49a7f48a8c8a72f9029b2060d520ec51aff2040a883199f800be0e23b6781`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 401.6 KB (401627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b883a1aaca55ac0ddb6ea87618bc903e2384d419dff78ab3111b8c7d7d00b`  
		Last Modified: Tue, 13 Jan 2026 23:01:57 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743279e77085da41e412ceadf20e068d4cec0712b4a4bd18027fcef50afff768`  
		Last Modified: Tue, 13 Jan 2026 23:01:36 GMT  
		Size: 388.4 KB (388395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e68fe60762d7163005606dc0a6a7fbd8f3ee3c40cdcf22e1d73fc2069932468`  
		Last Modified: Tue, 13 Jan 2026 23:01:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed2dd9d2d48687deb3f810080590e3bdace26052455ecf060f50f4e26da6797`  
		Last Modified: Tue, 13 Jan 2026 23:01:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb5d749a0778cebc1fd0e469ce99d6d9d425fdc7ecb308795e4527eebda1822`  
		Last Modified: Tue, 13 Jan 2026 23:01:34 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd1144ea2cb72a26c87648f037ccd9d5375d2f300af1c4ecca7781ad249222b`  
		Last Modified: Tue, 13 Jan 2026 23:02:10 GMT  
		Size: 224.3 MB (224314938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf834ae3de2bc4dc54c4704299b7aeca438edb1d40094664d1119fb1cfd27063`  
		Last Modified: Tue, 13 Jan 2026 23:01:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-4-jdk` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:80dab4c047002cb0563f2678383687f974209d30474d908d175610496863d0e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060785723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ec80dd35935a974e2ac8c5593f44c5930589f4c2f9631495f4573d90674f32`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:11:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:15 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 13 Jan 2026 23:11:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:21 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 23:11:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_windows-x64_bin.zip
# Tue, 13 Jan 2026 23:11:23 GMT
ENV JAVA_SHA256=03e913ca127ac00cd50269ad63a883ae5c879db36519d50788902f24576ebba7
# Tue, 13 Jan 2026 23:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 13 Jan 2026 23:11:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f681901ae8b8270ef4ad40879b419cd45d092d5d347a675266218039d5b88a0`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e725a46cf123e0204571db05eb82ce3a0b9811b0071f4bc3a34c999cda4e85`  
		Last Modified: Tue, 13 Jan 2026 23:12:29 GMT  
		Size: 490.4 KB (490380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3828c6449f875b1a7b5c838c648bd50d7dbe1b54339d49eb304d0b90d2eb9a`  
		Last Modified: Tue, 13 Jan 2026 23:12:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be3b9cd978ff8213b9dbb3d6cddec15a0700fbeee53a48e0162bf0cedff374`  
		Last Modified: Tue, 13 Jan 2026 23:12:28 GMT  
		Size: 337.7 KB (337707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8e2cbc3bc843dafebc4b5fe451a4e121b6f03cb720176dde8bc56828df64cb`  
		Last Modified: Tue, 13 Jan 2026 23:12:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569662b7e2bdea18d217081e2748cd88bcc8106ff4851b725c8b5c8e5ed7aab`  
		Last Modified: Tue, 13 Jan 2026 23:12:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740a63833dc6a0f63eb7e95f41c3cdcdf7d6bd1d1fb301f001f7f02b6057e5cc`  
		Last Modified: Tue, 13 Jan 2026 23:12:29 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49df72f0a4e284b1a974e63c6c1fb9463f932b89ae928ff693adec43b1f080aa`  
		Last Modified: Tue, 13 Jan 2026 23:12:41 GMT  
		Size: 224.3 MB (224290606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf713ff5ea24aa313f602af0e868e7ce2c03e1579d5465bf115f9d4c3d15ccb`  
		Last Modified: Tue, 13 Jan 2026 23:12:29 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
