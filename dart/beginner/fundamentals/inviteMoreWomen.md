Invite more Women

    bool inviteMoreWomen(List<int> attendees) {
      int menCount = attendees.where((gender) => gender == 1).length;
      int womenCount = attendees.where((gender) => gender == -1).length;
      return menCount > womenCount;
    }
