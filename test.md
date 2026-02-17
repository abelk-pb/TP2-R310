graph TD
    %% Définition des Acteurs
    Client([Client]):::externe
    Vendeur[Agent Vendeur]:::interne
    Financier[Service Financier]:::interne
    Secretariat[Secrétariat / Hotline]:::interne

    %% Flux d'informations
    Client -- "1. Critères de recherche" --> Vendeur
    Vendeur -. "2. Catalogue / Packs" .-> Client
    Client -- "3. Personnalisation" --> Vendeur
    Vendeur -- "4. Devis détaillé" --> Client
    Client -- "5. Accord + Infos persos" --> Vendeur
    Vendeur -- "6. Dossier pour paiement" --> Financier
    Client -- "7. Règlement (Acompte/Total)" --> Financier
    Financier -. "8. Facture / Reçu" .-> Client
    Financier -- "9. Confirmation paiement" --> Vendeur
    Vendeur -- "10. Pack Voyage (Billets/Bons)" --> Client
    Client -- "11. Demande assistance" --> Secretariat

    %% Styles
    classDef externe fill:#f9f,stroke:#333,stroke-width:2px
    classDef interne fill:#fff,stroke:#333,stroke-width:2px
